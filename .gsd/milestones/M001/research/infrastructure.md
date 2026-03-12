# Pesquisa: Infraestrutura Self-Hosted

**Relevância:** ALTA — Define toda a arquitetura de deploy e serviços

## Arquitetura Geral

```
┌─────────────┐     ┌──────────────────────────────────────────────┐
│   Vercel     │     │              VPS (Docker Compose)             │
│  (Frontend)  │────▶│                                              │
│  Next.js 15  │     │  ┌──────────┐  ┌─────────────────────────┐  │
└─────────────┘     │  │  Nginx   │  │  Supabase Self-Hosted   │  │
                    │  │  (proxy) │  │  ┌─────────────────────┐│  │
                    │  │  + SSL   │──│  │ PostgreSQL          ││  │
                    │  └──────────┘  │  │ GoTrue (Auth)       ││  │
                    │               │  │ PostgREST (API)     ││  │
                    │               │  │ Storage (S3-compat) ││  │
                    │               │  │ Realtime            ││  │
                    │               │  │ Kong (API Gateway)  ││  │
                    │               │  └─────────────────────┘│  │
                    │               └─────────────────────────┘  │
                    │                                              │
                    │  ┌─────────────────────────────┐             │
                    │  │  Claude Code Container      │             │
                    │  │  - Análise clínica (texto)  │             │
                    │  │  - OCR de exames (vision)   │             │
                    │  │  - Geração de insights      │             │
                    │  │  - API REST interna          │             │
                    │  │  - NÃO gera código           │             │
                    │  └─────────────────────────────┘             │
                    │                                              │
                    │  ┌──────────┐  ┌──────────────┐             │
                    │  │  Redis   │  │  PostHog     │             │
                    │  │  (cache) │  │  (analytics) │             │
                    │  └──────────┘  └──────────────┘             │
                    └──────────────────────────────────────────────┘
```

## Claude Code Container — Detalhes

### Propósito
Container Docker com Claude Code configurado exclusivamente para **análise de texto e geração de texto clínico**. Não gera código — apenas processa dados médicos e retorna insights estruturados.

### O que recebe (via API REST interna):
- Textos de formulários de check-in (peso, sintomas, adesão)
- Imagens de exames laboratoriais (para OCR via Vision)
- Documentos médicos (PDFs, fotos)
- Histórico do paciente (contexto para análise)
- Dados do SMI anterior (para comparação)

### O que retorna:
- Resumo clínico estruturado
- Valores extraídos de exames (OCR)
- Tendências identificadas
- Alertas clínicos
- Sugestão de orientação para o médico
- Score SMI calculado com justificativa

### Configuração do Container
```yaml
# docker-compose.yml (serviço claude-code)
claude-code:
  build: ./infra/claude-code
  environment:
    - ANTHROPIC_API_KEY=${ANTHROPIC_API_KEY}
    - CLAUDE_MODE=analysis  # texto/análise, não código
    - MAX_CONCURRENT=5
    - TIMEOUT_SECONDS=120
  volumes:
    - ./infra/claude-code/prompts:/app/prompts  # system prompts médicos
    - ./infra/claude-code/templates:/app/templates  # templates de resposta
  ports:
    - "127.0.0.1:3100:3100"  # API interna apenas (não exposta)
  restart: unless-stopped
  deploy:
    resources:
      limits:
        memory: 2G
```

### API Interna do Container
```
POST /api/analyze/checkin     → Analisa check-in mensal
POST /api/analyze/exam        → OCR + análise de exame laboratorial
POST /api/analyze/summary     → Gera resumo clínico completo
POST /api/analyze/orientation → Gera sugestão de orientação
POST /api/calculate/smi       → Calcula Score Metabólico Integrado
GET  /api/health              → Health check
```

### System Prompts Dedicados
O container terá prompts específicos em `/app/prompts/`:
- `checkin-analyzer.md` — Análise de formulário mensal
- `exam-ocr.md` — Extração de valores de exames
- `clinical-summary.md` — Geração de resumo clínico
- `orientation-draft.md` — Sugestão de orientação médica
- `smi-calculator.md` — Cálculo e justificativa do SMI

## Supabase Self-Hosted

### Componentes
| Serviço | Porta | Função |
|---------|-------|--------|
| PostgreSQL | 5432 | Banco de dados principal |
| GoTrue | 9999 | Autenticação (JWT) |
| PostgREST | 3000 | API REST automática |
| Storage | 5000 | Armazenamento de arquivos (exames, fotos) |
| Realtime | 4000 | Websockets (notificações) |
| Kong | 8000 | API Gateway |
| Studio | 3001 | Dashboard admin |

### Instalação
```bash
# Clone oficial do Supabase
git clone --depth 1 https://github.com/supabase/supabase
cd supabase/docker
cp .env.example .env
# Editar .env com senhas seguras
docker compose up -d
```

### Segurança
- RLS (Row Level Security) em TODAS as tabelas com dados médicos
- Criptografia em repouso (pgcrypto)
- Backups automáticos diários
- SSL/TLS obrigatório

## Nginx Reverse Proxy

### Configuração
```nginx
# API Supabase
server {
    listen 443 ssl;
    server_name api.metabolicmonitor.com.br;

    ssl_certificate /etc/letsencrypt/live/api.metabolicmonitor.com.br/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/api.metabolicmonitor.com.br/privkey.pem;

    location / {
        proxy_pass http://kong:8000;
    }
}

# Supabase Studio (admin only)
server {
    listen 443 ssl;
    server_name admin.metabolicmonitor.com.br;
    # IP whitelist para segurança
    allow YOUR_IP;
    deny all;

    location / {
        proxy_pass http://studio:3001;
    }
}
```

## Redis

### Uso
- Cache de sessões
- Fila de processamento de análises IA (Bull/BullMQ)
- Rate limiting da API
- Cache de SMI calculados

## PostHog Self-Hosted

### Instalação
```bash
git clone https://github.com/PostHog/posthog
cd posthog
docker compose -f docker-compose.hobby.yml up -d
```

## Requisitos Mínimos da VPS

| Recurso | Mínimo | Recomendado |
|---------|--------|-------------|
| CPU | 4 vCPUs | 8 vCPUs |
| RAM | 8 GB | 16 GB |
| Disco | 100 GB SSD | 200 GB NVMe |
| Banda | 1 Gbps | 1 Gbps |
| OS | Ubuntu 22.04 LTS | Ubuntu 24.04 LTS |

### Provedores Recomendados (Brasil)
| Provedor | Config Recomendada | Preço Estimado |
|----------|-------------------|----------------|
| Hetzner | CPX41 (8vCPU/16GB) | ~€25/mês |
| DigitalOcean | Premium 8GB | ~$68/mês |
| Contabo | VPS L | ~€13/mês |
| Oracle Cloud | Ampere A1 (free tier) | Grátis (limitado) |

## Decisões Derivadas

1. Supabase self-hosted para controle total dos dados médicos (LGPD)
2. Claude Code em container isolado com API REST interna
3. Container de IA NÃO exposto à internet — acessível apenas via rede Docker interna
4. Nginx como ponto único de entrada com SSL
5. Redis para filas de processamento (análises IA são assíncronas)
6. Backups automáticos do PostgreSQL (dados médicos são críticos)
7. Scripts de instalação automatizados em `infra/`
8. PostHog self-hosted para não enviar dados de uso para terceiros
