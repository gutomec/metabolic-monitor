# M001: Metabolic Monitor — MVP

**Vision:** Plataforma funcional onde paciente faz check-in mensal, upload de exames → Claude Code container na VPS analisa e gera resumo clínico → médico aprova/envia orientação. SMI (Score Metabólico Integrado) trackeia evolução. Landing page captura leads e converte em assinantes. Painel médico com fila organizada. Tudo self-hosted (Supabase + Claude Code + PostHog) em VPS com Docker Compose.

**Success Criteria:**
- VPS provisionada com todos os serviços (Supabase, Claude Code, Nginx, Redis, PostHog)
- Landing page converte visitantes em leads/assinantes
- Checkout processa pagamento recorrente
- Paciente preenche check-in mensal completo
- Exames são processados via OCR (Claude Code Vision)
- Claude Code container gera resumo clínico estruturado
- SMI calculado com 6 domínios e histórico
- Painel médico funciona com fila + aprovação
- Dashboard do paciente mostra evolução
- PWA funciona em mobile
- LGPD compliance implementado

## Slices

- [ ] **S01: Infrastructure** `risk:high` `depends:[]`
  > After: VPS provisionada com Docker Compose rodando: Supabase self-hosted (PostgreSQL, GoTrue, PostgREST, Storage, Realtime, Kong), Claude Code container com API REST interna (análise de texto/mídia, não código), Nginx reverse proxy com SSL (Let's Encrypt), Redis (cache + filas), PostHog self-hosted. Scripts de instalação automatizados em infra/. Health checks funcionando

- [ ] **S02: Foundation** `risk:low` `depends:[S01]`
  > After: Next.js 15 configurado apontando para Supabase self-hosted, auth (médico + paciente), schema do banco com tabelas clínicas, layout base responsivo, design tokens médicos, RLS policies para dados sensíveis

- [ ] **S03: Patient Check-in** `risk:medium` `depends:[S02]`
  > After: Formulário mensal estruturado (peso, medidas, fotos, sintomas, adesão, medicação). Upload de exames laboratoriais com OCR via Claude Code container. Histórico de check-ins. Validação de dados clínicos

- [ ] **S04: SMI Engine** `risk:high` `depends:[S03]`
  > After: Score Metabólico Integrado calculado com 6 domínios (composição corporal, glicometabolismo, inflamação, perfil lipídico, eixo hormonal, micronutrientes). Fórmula ponderada. Histórico de evolução. Visualização radar chart

- [ ] **S05: AI Clinical Summary** `risk:high` `depends:[S03,S04]`
  > After: Claude Code container analisa dados do check-in + exames + SMI → gera resumo clínico estruturado (evolução, tendências, alertas, sugestões). Comparação com meses anteriores. Sugestão de orientação para o médico aprovar. Fila assíncrona via Redis/BullMQ

- [ ] **S06: Doctor Panel** `risk:medium` `depends:[S05]`
  > After: Painel médico com fila de pacientes organizada por prioridade (alertas primeiro). Visualização do resumo IA. Botões aprovar/editar/enviar. Histórico de orientações. Tempo médio por paciente < 5 min

- [ ] **S07: Patient Dashboard** `risk:low` `depends:[S04,S06]`
  > After: Dashboard do paciente com SMI visual (radar chart), evolução de peso, metas mensais, histórico de orientações recebidas, próximo check-in, conquistas de evolução

- [ ] **S08: Landing + Checkout** `risk:medium` `depends:[S02]`
  > After: Landing page com hero, benefícios, SMI demo, prova social, pricing, FAQ. Formulário inteligente (já é paciente? / novo). Checkout Stripe + Asaas. Plano Essencial R$347/mês. CRM para leads não convertidos

- [ ] **S09: Polish + PWA** `risk:low` `depends:[S03,S06,S07,S08]`
  > After: PWA manifest + service worker. Responsividade mobile. Loading states, error boundaries. Notificações de check-in. Disclaimers CFM. Termo de adesão digital. Meta tags SEO. PostHog analytics integrado

## Boundary Map

### S01 → S02
**S01 Produces:**
- `infra/docker-compose.yml` → todos os serviços
- `infra/claude-code/` → Dockerfile, prompts, API wrapper
- `infra/nginx/` → configs, SSL
- `infra/scripts/setup.sh` → provisioning automatizado
- Supabase acessível via URL da VPS
- Claude Code container com API interna em :3100
- Redis em :6379

**S02 Consumes:**
- URLs do Supabase self-hosted de S01
- Variáveis de ambiente de conexão

### S02 → S03
**S02 Produces:**
- `src/lib/supabase.ts` → createClient(), auth helpers
- `src/types/database.ts` → Database type definitions
- Schema SQL: profiles, patients, doctors, clinics
- RLS policies para dados sensíveis
- Layout responsivo com sidebar médica

**S03 Consumes:**
- Supabase client + types de S02
- Layout base de S02
- Auth context (patient role)
- Claude Code container API de S01 (para OCR)

### S03 → S04
**S03 Produces:**
- `src/lib/checkin.ts` → submitCheckin(), getHistory()
- `src/lib/exam-ocr.ts` → extractExamData() via Claude Code container
- Tabelas: checkins, exam_results, exam_values
- Dados estruturados de exames laboratoriais

**S04 Consumes:**
- Dados de checkins e exames de S03
- Valores laboratoriais extraídos para cálculo do SMI

### S04 → S05
**S04 Produces:**
- `src/lib/smi.ts` → calculateSMI(), getDomainScores()
- Tabela smi_scores (patient_id, date, scores por domínio)
- Score atual + histórico

**S05 Consumes:**
- SMI scores de S04
- Dados de checkin de S03
- Exames de S03
- Claude Code container API de S01

### S05 → S06
**S05 Produces:**
- `src/lib/ai-summary.ts` → requestClinicalSummary() via Claude Code container
- `src/lib/ai-suggestion.ts` → requestOrientation() via Claude Code container
- `src/lib/queue.ts` → BullMQ jobs para processamento assíncrono
- Tabela clinical_summaries (patient_id, checkin_id, summary, suggestion, status)

**S06 Consumes:**
- Clinical summaries de S05
- Patient data de S02/S03
- SMI de S04

### S06 → S07
**S06 Produces:**
- `src/lib/orientation.ts` → approveOrientation(), sendToPatient()
- Tabela orientations (doctor_id, patient_id, content, sent_at)

**S07 Consumes:**
- Orientações aprovadas de S06
- SMI de S04
- Checkin history de S03

### S08 (independente de S03-S07)
**S08 Produces:**
- Landing page em `/`
- Checkout flow em `/checkout`
- `src/lib/billing.ts` → Stripe/Asaas integration
- `src/lib/crm.ts` → lead management
- Tabela leads (name, email, phone, status, source)
