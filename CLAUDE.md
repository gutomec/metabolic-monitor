# Metabolic Monitor — Plataforma de Monitoramento Terapêutico Metabólico

## Identidade
Plataforma SaaS médica de Remote Therapeutic Monitoring (RTM) para saúde metabólica.
Pacientes enviam dados mensais (peso, exames, sintomas) → IA organiza e gera resumo clínico → Médico aprova/ajusta → Paciente recebe orientação.
Score Metabólico Integrado (SMI) como motor clínico central.

## Stack
- **Frontend:** Next.js 15 (App Router), TypeScript, Tailwind CSS, shadcn/ui
- **Backend:** Supabase Self-Hosted (Auth, Database, Storage, Edge Functions) — VPS
- **IA Engine:** Claude Code em container Docker na VPS — recebe textos/mídias/documentos via API interna, analisa e gera insights clínicos (NÃO gera código, apenas texto/análise)
- **OCR/Exames:** Claude Code container (Vision) — leitura de exames laboratoriais
- **Pagamento:** Stripe (cartão) + Asaas (Pix/Boleto)
- **Deploy Frontend:** Vercel
- **Deploy Backend:** VPS (Docker Compose: Supabase + Claude Code container + Nginx + Redis)
- **Analytics:** PostHog (self-hosted na VPS)

## Infraestrutura VPS
Todos os serviços backend rodam em uma VPS com Docker Compose:
- **Supabase Self-Hosted:** PostgreSQL, GoTrue (auth), PostgREST, Storage, Realtime, Kong
- **Claude Code Container:** Container Docker com Claude Code configurado para análise clínica (texto/mídia, não código). Expõe API REST interna para receber formulários/documentos e retornar insights
- **Nginx:** Reverse proxy + SSL (Let's Encrypt)
- **Redis:** Cache + filas de processamento
- **PostHog:** Analytics self-hosted
- Scripts de instalação em `infra/` para provisionar tudo automaticamente

## Decision Levels
- **L1 (autonomia total):** implementação, testes, refactoring, UI components
- **L2 (informar depois):** nova dependência, schema migration, API route
- **L3 (perguntar antes):** mudança de arquitetura, lógica clínica do SMI, compliance médico, billing

## Routing Table
| Request | Handler |
|---------|---------|
| Código/implementação | executor agent |
| UI/UX design | designer agent |
| Lógica clínica/SMI | architect agent → confirmar com usuário |
| Compliance médico | consultar .claude/rules/ |
| Marketing/copy | consultar strategy/ docs |
| Pesquisa científica | document-specialist agent |

## Code Standards
- Variáveis e código em inglês
- Comentários e UI em português (pt-BR)
- UTF-8 sempre
- Acentuação correta em português
- Components: PascalCase | utils: camelCase | constants: UPPER_SNAKE
- Supabase types auto-generated
- Server Components por padrão, Client Components só quando necessário

## Critical Rules
1. **LGPD + CFM:** Dados de saúde são sensíveis. Consentimento explícito obrigatório. Criptografia em repouso.
2. **IA não prescreve:** IA gera resumos e sugestões. Médico SEMPRE valida. Nunca gerar conduta autônoma.
3. **Não é teleconsulta:** É monitoramento terapêutico. Disclaimers obrigatórios em toda interface.
4. **Exames:** OCR extrai dados, mas médico confirma valores. Nunca confiar cegamente no OCR.
5. **Score Metabólico:** Fórmula definida em .brain/. Qualquer mudança é L3.

## Anti-Patterns
- ❌ IA dando diagnóstico ou conduta sem aprovação médica
- ❌ Armazenar dados médicos sem criptografia
- ❌ Permitir paciente novo sem consulta prévia
- ❌ Resposta ilimitada por WhatsApp (escopo definido)
- ❌ Hardcoded clinical thresholds (usar config)

## Context Loading
- Domínio clínico: `.brain/BRAIN.yaml`
- Compliance: `.claude/rules/medical-compliance.md`
- Score Metabólico: `.claude/rules/smi-score.md`
- Estado do projeto: `.gsd/STATE.md`
- Estratégia comercial: `strategy/`
- Pesquisa: `.gsd/milestones/M001/research/`
