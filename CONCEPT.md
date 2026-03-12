# Metabolic Monitor — Conceito do Produto

## O que é
Plataforma de **Monitoramento Terapêutico Metabólico Digital** baseada em Remote Therapeutic Monitoring (RTM). Permite que médicos acompanhem pacientes remotamente com análise de IA, transformando dados clínicos em insights acionáveis.

## O Problema
- Pacientes perdem adesão entre consultas (média 40-60% de abandono)
- Dados de exames ficam desorganizados em papéis e PDFs
- Médico não consegue escalar atendimento sem perder qualidade
- Não existe plataforma de monitoramento metabólico médico estruturado no Brasil
- Ajustes de dose/protocolo atrasam por falta de acompanhamento contínuo

## A Solução

### Para o Paciente
1. **Check-in mensal estruturado** — preenche formulário com peso, medidas, sintomas, adesão, medicação
2. **Upload de exames** — fotos/PDFs de exames laboratoriais processados por OCR
3. **Score Metabólico Integrado (SMI)** — score de 0-100 avaliando 6 domínios metabólicos
4. **Dashboard de evolução** — gráficos, metas, conquistas, histórico
5. **Orientações personalizadas** — recebe feedback médico estruturado todo mês

### Para o Médico
1. **Fila organizada** — pacientes ordenados por prioridade (alertas primeiro)
2. **Resumo IA** — Claude Code analisa dados e gera resumo clínico estruturado
3. **Aprovar em 3-5 minutos** — lê resumo, ajusta se necessário, envia
4. **Receita recorrente** — R$347/paciente/mês sem aumentar carga de trabalho
5. **Histórico completo** — evolução de cada paciente ao longo do tempo

## Score Metabólico Integrado (SMI)

O coração científico da plataforma. Avalia 6 domínios:

| Domínio | Peso | Marcadores |
|---------|------|------------|
| Composição Corporal | 25% | IMC, circunferência abdominal, % gordura, gordura visceral |
| Metabolismo Glicêmico | 20% | Glicemia, insulina, HOMA-IR, HbA1c |
| Inflamação Metabólica | 15% | PCR-us, ferritina, ácido úrico |
| Perfil Lipídico | 15% | HDL, triglicerídeos, TG/HDL, LDL |
| Eixo Hormonal | 15% | Testosterona, SHBG, estradiol, cortisol, TSH |
| Micronutrientes | 10% | Vitamina D, B12, magnésio, zinco |

**Interpretação:**
- 85-100: Saúde metabólica ótima
- 70-84: Boa saúde metabólica
- 55-69: Risco metabólico moderado
- 40-54: Disfunção metabólica
- <40: Alto risco metabólico

## Arquitetura de IA

**Claude Code em container Docker na VPS** — configurado exclusivamente para análise de texto e mídia médica (não gera código). Recebe dados via API REST interna:

- Análise de check-ins mensais
- OCR de exames laboratoriais (Vision)
- Geração de resumos clínicos
- Sugestões de orientação
- Cálculo e justificativa do SMI

**Regra inviolável:** IA gera sugestões → Médico SEMPRE aprova antes de enviar ao paciente.

## Fluxo do Sistema

```
Landing Page → Lead Capture → Formulário Filtro
                                    │
                    ┌───────────────┤
                    ▼               ▼
              Já é paciente    Novo paciente
                    │               │
                    ▼               ▼
               Checkout      Agendar consulta
                    │
                    ▼
            Área do Paciente
                    │
                    ▼ (todo mês)
            Check-in Mensal
            (peso, sintomas, exames)
                    │
                    ▼
         Claude Code Container
         (analisa, OCR, resume)
                    │
                    ▼
            Painel Médico
            (fila de pacientes)
                    │
                    ▼
         Médico aprova/edita
                    │
                    ▼
         Paciente recebe orientação
         + SMI atualizado
```

## Modelo de Negócio

### Fase 1 — B2C (Dr. Paulo)
- **Plano Essencial:** R$347/mês (mínimo 3 meses)
- **Meta:** 50-200 pacientes
- **Receita projetada:** R$17.350 - R$69.400/mês

### Fase 2 — B2B (outros médicos)
- **Assinatura médica:** R$500-1.500/mês
- **Acesso à plataforma completa para seus pacientes**

### Fase 3 — White-label
- **Clínicas licenciam com sua marca**
- **Sob consulta**

## Posicionamento

**NÃO é:**
- ❌ App de dieta
- ❌ Teleconsulta online
- ❌ Coaching de saúde
- ❌ Prontuário eletrônico

**É:**
- ✅ Monitoramento Terapêutico Metabólico Digital
- ✅ Infraestrutura médica digital para medicina metabólica de precisão
- ✅ Remote Therapeutic Monitoring (RTM) com IA

## Base Científica

4 pilares:
1. **Remote Therapeutic Monitoring** — monitoramento contínuo da resposta terapêutica
2. **Behavioral Medicine** — check-ins regulares aumentam adesão ao tratamento
3. **Digital Health Interventions** — intervenções digitais guiadas por médico
4. **Precision Lifestyle Medicine** — ajustes baseados em dados individuais

## Áreas Cobertas (Saúde Metabólica Completa)

- Emagrecimento e obesidade
- Composição corporal
- Eixo hormonal
- Inflamação metabólica
- Saúde mitocondrial / energia
- Queda de cabelo metabólica
- Lipedema e inflamação crônica
- Performance metabólica

## Stack Técnico

- **Frontend:** Next.js 15 + TypeScript + Tailwind + shadcn/ui → Vercel
- **Backend:** Supabase Self-Hosted → VPS Docker
- **IA:** Claude Code container Docker → VPS (API REST interna)
- **Pagamento:** Stripe + Asaas
- **Infra:** Docker Compose (Supabase + Claude Code + Nginx + Redis + PostHog)
