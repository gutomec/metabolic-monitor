# Memory — Metabolic Monitor

## Architectural Decisions
- Stack: Next.js 15 + Supabase Self-Hosted + Claude Code Container (VPS) + Stripe/Asaas
- IA: Claude Code em container Docker, análise de texto/mídia apenas, API REST interna
- Toda infra backend em VPS com Docker Compose
- Frontend no Vercel
- SMI (Score Metabólico Integrado) é o motor clínico central — 6 domínios ponderados
- IA NUNCA dá conduta autônoma — médico sempre valida

## Project Origin
- Ideia do Dr. Paulo Almeida (nutrólogo) para monitoramento remoto de pacientes
- Conceito baseado em Remote Therapeutic Monitoring (RTM)
- Fase 1: B2C (pacientes do Dr. Paulo), Fase 2: B2B (outros médicos), Fase 3: White-label
- Pricing: R$347/mês, mínimo 3 meses

## Key Files
- Conceito completo: `CONCEPT.md`
- Score Metabólico: `.claude/rules/smi-score.md`
- Compliance médico: `.claude/rules/medical-compliance.md`
- Infra: `.gsd/milestones/M001/research/infrastructure.md`
- Strategy: `strategy/sales-pitch.md`, `strategy/landing-page-copy.md`
