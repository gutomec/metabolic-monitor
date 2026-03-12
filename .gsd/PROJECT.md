# Metabolic Monitor

## Vision
Plataforma SaaS de Monitoramento Terapêutico Metabólico Digital (Remote Therapeutic Monitoring) que permite médicos acompanharem pacientes remotamente com análise de IA. Pacientes enviam dados mensais, IA organiza e gera resumos clínicos estruturados, médico aprova/ajusta em 3-5 minutos por paciente. Score Metabólico Integrado (SMI) como motor clínico central avaliando 6 domínios metabólicos.

## Problem
- Pacientes perdem adesão entre consultas presenciais
- Médicos não têm ferramenta estruturada para monitoramento remoto
- Dados de exames ficam desorganizados
- Não existe plataforma de monitoramento metabólico médico no Brasil
- Ajustes de dose/protocolo atrasam por falta de acompanhamento

## Solution
Plataforma onde:
1. Paciente preenche check-in mensal (peso, medidas, sintomas, exames)
2. IA analisa dados, extrai informações de exames, compara histórico
3. IA gera resumo clínico + sugestão de orientação
4. Médico revisa fila de pacientes, aprova/edita, envia orientação
5. SMI (Score Metabólico Integrado) trackeia evolução em 6 domínios
6. Dashboard do paciente mostra evolução e metas

## Target Users
- **Fase 1:** Dr. Paulo Almeida (nutrólogo) + seus pacientes
- **Fase 2:** Outros nutrólogos e endocrinologistas
- **Fase 3:** Clínicas metabólicas, médicos do esporte, programas corporativos

## Stack
- **Frontend:** Next.js 15 (App Router) + TypeScript + Tailwind CSS + shadcn/ui → Vercel
- **Backend:** Supabase Self-Hosted (PostgreSQL, GoTrue, PostgREST, Storage, Realtime) → VPS Docker
- **IA Engine:** Claude Code em container Docker na VPS — configurado para análise de texto/mídia/documentos (não código). Recebe dados via API REST interna e retorna insights clínicos estruturados
- **OCR:** Claude Code container (Vision) para leitura de exames laboratoriais
- **Pagamento:** Stripe (cartão) + Asaas (Pix/Boleto)
- **Infra VPS:** Docker Compose (Supabase + Claude Code + Nginx + Redis + PostHog)
- **Analytics:** PostHog self-hosted na VPS

## Business Model
- **B2C:** Pacientes pagam R$347/mês (Plano Essencial)
- **B2B (futuro):** Médicos pagam R$500-1.500/mês para usar plataforma
- **White-label (futuro):** Clínicas licenciam com sua marca

## Success Criteria (MVP)
- [ ] Landing page captura leads com formulário inteligente
- [ ] Checkout processa pagamento recorrente (Stripe/Asaas)
- [ ] Paciente preenche check-in mensal estruturado
- [ ] Upload e OCR de exames laboratoriais funciona
- [ ] IA gera resumo clínico estruturado por paciente
- [ ] SMI calculado e exibido com 6 domínios
- [ ] Painel médico com fila de pacientes organizada
- [ ] Médico aprova/edita/envia orientação em < 5 min
- [ ] Dashboard do paciente mostra evolução e metas
- [ ] PWA funciona em mobile
- [ ] Compliance LGPD + disclaimers CFM implementados

## Risks
| Risk | Impact | Mitigation |
|------|--------|------------|
| IA gerar conduta incorreta | CRÍTICO | Médico SEMPRE valida. IA só sugere |
| LGPD / dados sensíveis | ALTO | Criptografia, consentimento, RLS |
| OCR falhar em exames | MÉDIO | Fallback para input manual |
| Baixa adesão ao check-in | MÉDIO | Gamificação via SMI + notificações |
| Regulação CFM mudar | MÉDIO | Disclaimers, termo de adesão |

## References
- Remote Therapeutic Monitoring (RTM) - CPT codes 98975-98981
- Digital Health Weight Loss Interventions
- Lifestyle Medicine Digital Programs
- LGPD Art 11 (dados sensíveis de saúde)
- CFM Resolução 2.314/2022 (telemedicina)
