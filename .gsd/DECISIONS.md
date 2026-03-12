# Decision Log — Metabolic Monitor

## D001: Stack Principal
**Data:** 2026-03-12
**Decisão:** Next.js 15 + Supabase + Claude API + Stripe/Asaas
**Razão:** Mesmo stack validado no Reforço IA Kids. Supabase oferece RLS nativo (essencial para dados médicos). Claude Vision para OCR de exames.

## D002: Modelo de Negócio Fase 1
**Data:** 2026-03-12
**Decisão:** B2C — Paciente paga R$347/mês, plano mínimo 3 meses
**Razão:** Preço abaixo de R$500 mantém acessibilidade. Mínimo 3 meses reduz churn. Van Westendorp estimado: R$200-400 zona ideal.

## D003: IA como Organizador, Não Decisor
**Data:** 2026-03-12
**Decisão:** IA gera resumos e sugestões. Médico SEMPRE valida antes de enviar ao paciente.
**Razão:** Compliance CFM + segurança do paciente. IA não pode dar conduta médica autônoma.

## D004: Score Metabólico Integrado (SMI)
**Data:** 2026-03-12
**Decisão:** SMI com 6 domínios ponderados (composição corporal 25%, glicometabolismo 20%, inflamação 15%, lipídico 15%, hormonal 15%, micronutrientes 10%)
**Razão:** Baseado em evidência científica de medicina metabólica. Cobre os principais eixos de saúde metabólica.

## D005: Posicionamento como RTM
**Data:** 2026-03-12
**Decisão:** Apresentar como "Monitoramento Terapêutico Metabólico Digital", não como "consulta online" ou "app de dieta"
**Razão:** Reduz risco jurídico, eleva percepção de valor, alinha com literatura científica (Remote Therapeutic Monitoring).

## D006: Filtro de Entrada
**Data:** 2026-03-12
**Decisão:** Paciente novo precisa de consulta prévia (presencial ou telemedicina) antes de entrar no monitoramento
**Razão:** CFM exige avaliação médica antes de acompanhamento. Protege médico e paciente juridicamente.

## D007: OCR de Exames
**Data:** 2026-03-12
**Decisão:** Claude Vision API para extração de dados de exames laboratoriais
**Razão:** Melhor qualidade de OCR contextual (entende o que está lendo). Fallback para input manual se OCR falhar.

## D008: Compliance LGPD
**Data:** 2026-03-12
**Decisão:** Dados de saúde com criptografia em repouso, RLS no Supabase, consentimento explícito, termo de adesão digital
**Razão:** LGPD Art 11 classifica dados de saúde como sensíveis. Multa pode chegar a 2% do faturamento.

## D009: Arquitetura Multi-tenant (futuro)
**Data:** 2026-03-12
**Decisão:** Schema já preparado para multi-tenant (doctor_id, clinic_id) mesmo no MVP
**Razão:** Fase 2 prevê outros médicos usando a plataforma. Melhor preparar o schema desde o início.

## D010: PWA First
**Data:** 2026-03-12
**Decisão:** PWA ao invés de app nativo
**Razão:** Menor custo de desenvolvimento. Sem necessidade de aprovação em stores. Paciente acessa pelo celular sem instalar app.

## D011: Lançamento em Fases
**Data:** 2026-03-12
**Decisão:** Fase 1 (pacientes Dr. Paulo, 3 meses) → Fase 2 (outros médicos) → Fase 3 (nacional)
**Razão:** Validar modelo operacional antes de escalar. Evitar caos jurídico/operacional.

## D012: Não Incluir Chat Ilimitado
**Data:** 2026-03-12
**Decisão:** Sem chat/WhatsApp ilimitado. Canal de dúvidas com escopo definido e resposta em até 48h úteis.
**Razão:** Evitar virar "plantão de WhatsApp". Proteger tempo do médico. Manter escalabilidade.

## D013: Gamificação via SMI
**Data:** 2026-03-12
**Decisão:** Usar evolução do SMI como mecanismo de engajamento (metas mensais, conquistas, comparativo)
**Razão:** Paciente quer ver progresso mensurável. SMI cria ciclo de engajamento natural.

## D014: Landing com Formulário Inteligente
**Data:** 2026-03-12
**Decisão:** Landing page com dois caminhos: "Já sou paciente" (direto para checkout) e "Quero iniciar" (redireciona para consulta)
**Razão:** Evitar aceitar paciente sem avaliação prévia. Aumenta ticket médio com consulta + monitoramento.

## D016: Infraestrutura Self-Hosted (VPS)
**Data:** 2026-03-12
**Decisão:** Toda infraestrutura backend self-hosted em VPS com Docker Compose (Supabase + Claude Code container + Nginx + Redis + PostHog)
**Razão:** Controle total sobre dados médicos sensíveis (LGPD). Evita dependência de serviços cloud para dados de saúde. Supabase self-hosted permite customização completa. Claude Code container isolado na rede interna.

## D017: Claude Code Container como Motor de IA
**Data:** 2026-03-12
**Decisão:** Claude Code rodando em container Docker na VPS, acessado via API REST interna, configurado para análise de texto/mídia (não código)
**Razão:** Claude Code é mais poderoso que a API direta para análise contextual. Pode receber textos, mídias, documentos. Container isolado garante segurança. API interna não exposta à internet.

## D018: Supabase Self-Hosted
**Data:** 2026-03-12
**Decisão:** Supabase self-hosted ao invés de Supabase Cloud
**Razão:** Dados médicos sensíveis devem ficar em infra própria. Self-hosted permite backup personalizado, criptografia customizada e compliance LGPD total.

## D015: CRM para Leads
**Data:** 2026-03-12
**Decisão:** Leads não convertidos vão para CRM. Secretária faz follow-up.
**Razão:** Funil perpétuo. Leads são ativos valiosos para conversão futura.
