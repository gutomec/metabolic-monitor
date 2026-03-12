# Medical Compliance Rules

## LGPD — Lei Geral de Proteção de Dados
- **Art 11:** Dados de saúde são SENSÍVEIS. Tratamento apenas com consentimento EXPLÍCITO
- Criptografia em repouso obrigatória para dados clínicos
- Paciente pode solicitar exclusão de dados a qualquer momento
- Controlador deve nomear DPO (Data Protection Officer)
- Incidentes de segurança devem ser reportados à ANPD em 72h

## CFM — Conselho Federal de Medicina
- **Resolução 2.314/2022:** Regulamenta telemedicina no Brasil
- Monitoramento terapêutico NÃO é teleconsulta — é acompanhamento de tratamento já iniciado
- Paciente PRECISA de consulta prévia (presencial ou telemedicina) antes de monitoramento
- Prontuário eletrônico deve seguir normas do CFM
- Médico é o responsável técnico — IA é ferramenta auxiliar

## Disclaimers Obrigatórios
Toda interface deve conter:
1. "Este serviço não substitui consulta médica presencial"
2. "Em caso de emergência, procure atendimento presencial"
3. "As orientações são baseadas nos dados informados pelo paciente"
4. "Ajustes de medicação só são válidos após aprovação do médico responsável"

## Termo de Adesão
Paciente deve assinar digitalmente antes de usar a plataforma:
- Consentimento para coleta de dados de saúde
- Ciência de que não é serviço de emergência
- Autorização para processamento por IA (com supervisão médica)
- Escopo do serviço (monitoramento, não consulta)
- Política de cancelamento

## IA — Regras Invioláveis
1. IA NUNCA gera diagnóstico
2. IA NUNCA prescreve medicação
3. IA NUNCA envia orientação sem aprovação médica
4. IA gera RESUMOS e SUGESTÕES — médico DECIDE
5. Se IA detectar situação de risco, ALERTA o médico (não o paciente)

## Dados de Exames
- OCR extrai valores, mas médico CONFIRMA antes de usar clinicamente
- Valores laboratoriais devem mostrar range de referência
- Histórico de exames deve ser rastreável
- Upload de exames deve ser armazenado com criptografia

## RLS (Row Level Security)
- Paciente acessa APENAS seus dados
- Médico acessa APENAS dados dos seus pacientes
- Admin da clínica acessa dados da clínica
- Nenhum paciente vê dados de outro paciente — JAMAIS
