# Fundamentos Científicos da Plataforma Digital de Monitoramento Metabólico

**Versão:** 1.0
**Data:** Março de 2026
**Classificação:** Documento de Base Científica — Milestone M001
**Autores:** Equipe de Pesquisa e Desenvolvimento Clínico

---

## Sumário

1. [Remote Therapeutic Monitoring (RTM)](#1-remote-therapeutic-monitoring-rtm)
2. [Intervenções Digitais para Obesidade](#2-intervenções-digitais-para-obesidade)
3. [Medicina Comportamental e Adesão](#3-medicina-comportamental-e-adesão)
4. [Sistemas de Pontuação de Saúde Metabólica](#4-sistemas-de-pontuação-de-saúde-metabólica)
5. [Inteligência Artificial em Suporte à Decisão Clínica](#5-inteligência-artificial-em-suporte-à-decisão-clínica)
6. [OCR para Resultados Laboratoriais](#6-ocr-para-resultados-laboratoriais)
7. [Engajamento do Paciente via Dashboards](#7-engajamento-do-paciente-via-dashboards)
8. [Programas Digitais de Medicina do Estilo de Vida](#8-programas-digitais-de-medicina-do-estilo-de-vida)
9. [Marco Regulatório Brasileiro](#9-marco-regulatório-brasileiro)
10. [Score Metabólico Integrado (SMI)](#10-score-metabólico-integrado-smi)
11. [Implicações para o Produto](#11-implicações-para-o-produto)
12. [Referências](#12-referências)

---

## 1. Remote Therapeutic Monitoring (RTM)

### 1.1 Definição e Contexto

O Remote Therapeutic Monitoring (RTM) é uma modalidade de cuidado em saúde digital que permite a coleta, transmissão e análise de dados terapêuticos do paciente fora do ambiente clínico tradicional, com acompanhamento ativo por profissional de saúde qualificado. Diferencia-se do Remote Patient Monitoring (RPM) por focar em dados terapêuticos — incluindo adesão a medicamentos, dor, qualidade de vida e resposta a intervenções comportamentais — em vez de dados fisiológicos contínuos como frequência cardíaca e saturação de oxigênio (Makhni et al., 2021; CMS, 2022).

O RTM foi formalizado como modalidade reembolsável pelo Centers for Medicare & Medicaid Services (CMS) dos Estados Unidos em 2022, reconhecendo que o monitoramento entre consultas é componente essencial do cuidado contínuo e não apenas um complemento tecnológico (APTA, 2023).

### 1.2 Códigos CPT (98975–98981)

O conjunto de códigos CPT aprovado pela American Medical Association (AMA) para RTM compreende seis códigos distintos, cada um refletindo uma etapa do ciclo de monitoramento terapêutico:

| Código CPT | Descrição | Remuneração Média (EUA, 2024) |
|------------|-----------|-------------------------------|
| **98975** | Configuração inicial e educação do paciente sobre uso do dispositivo | USD 19,73 |
| **98976** | Dispositivo de monitoramento respiratório — coleta de ≥16 dias por mês | USD 48,82 |
| **98977** | Dispositivo de monitoramento musculoesquelético — coleta de ≥16 dias | USD 48,82 |
| **98978** | Dispositivo de monitoramento comportamental/cognitivo — coleta de ≥16 dias | USD 48,82 |
| **98980** | Gestão terapêutica — primeiros 20 minutos/mês (requer comunicação interativa) | USD 50,18 |
| **98981** | Gestão terapêutica — cada 20 minutos adicionais/mês | USD 39,14 |

**Requisitos de elegibilidade:** O código 98975 pode ser faturado uma única vez por prestador, quando ao menos 16 dias de dados tenham sido coletados em dispositivo médico. Os códigos 98980 e 98981 exigem ao menos uma comunicação interativa ao vivo com o paciente ou cuidador durante o mês calendário (Tenovi, 2024; ThoroughCare, 2025).

Em 2026, a AMA aprovou dois novos códigos RTM, expandindo ainda mais o escopo de monitoramento reembolsável — sinal inequívoco de que o modelo é considerado clinicamente válido e economicamente sustentável pelo sistema regulatório norte-americano (CMS, 2026).

### 1.3 Base de Evidências e Desfechos

A implementação do RTM em doenças reumáticas e musculoesqueléticas demonstrou capacidade de identificar não-adesão, monitorar atividade da doença e capturar mudanças em domínios-chave como fadiga, dor, função física e saúde mental (Michaud et al., 2024; PMC10972608). A infraestrutura desenvolvida pelo ArthritisPower demonstrou que a coleta contínua de dados entre consultas permite intervenções mais precoces e personalizadas.

Uma revisão sistemática de 2024 publicada no npj Digital Medicine analisou 29 estudos de 16 países e confirmou que o RPM/RTM impacta positivamente desfechos de segurança do paciente, adesão, qualidade de vida e custos durante a transição do cuidado (npj Digital Medicine, 2024).

**Relevância para o contexto de saúde metabólica:** O monitoramento terapêutico remoto é diretamente aplicável ao manejo de obesidade e síndrome metabólica, condições que exigem ajustes frequentes e monitoramento longitudinal de múltiplos parâmetros. A coleta sistemática de dados entre consultas reduz o viés de rememoração, permite identificação precoce de deterioração metabólica e fundamenta decisões clínicas baseadas em tendências reais, e não em snapshots episódicos.

---

## 2. Intervenções Digitais para Obesidade

### 2.1 Panorama das Meta-análises Recentes

A literatura científica sobre intervenções digitais para obesidade expandiu-se consideravelmente entre 2023 e 2025, com múltiplas revisões sistemáticas e meta-análises fornecendo evidências quantificadas de eficácia.

**Meta-análise de e-Health e m-Health (MDPI Nutrients, 2025):**
Uma meta-análise abrangente publicada em 2025, com buscas até outubro de 2024 em três bases de dados (Medline, Web of Science, Scopus), avaliou RCTs de intervenções digitais comparadas a grupos-controle em adultos com sobrepeso ou obesidade. Os principais achados foram:

- Intervenções digitais vs. nenhum cuidado: MD = −4,32 kg (IC 95%: −5,08 a −3,57 kg)
- Intervenções digitais vs. cuidado face a face: MD = −0,12 kg (IC 95%: −0,64 a 0,41 kg)
- Aplicativos móveis: redução significativa no peso corporal (MD = −1,32 kg; I² = 82%)
- Intervenções digitais de longa duração: MD = −1,13 kg (I² = 76%)

**Revisão com Component Network Meta-Analysis (JMIR, 2025):**
O estudo identificou os componentes dos programas digitais que mais efetivamente apoiam a perda de peso. Os elementos com maior impacto foram: automonitoramento contínuo, feedback personalizado, suporte comportamental estruturado e metas progressivas. A revisão analisou dados de buscas até 2024, incluindo dezenas de RCTs (PMC12141966).

**Umbrella Review (PMC10482795, 2023):**
Uma revisão de revisões sistemáticas confirmou que intervenções de eHealth são superiores a grupos-controle ou sem cuidado, e comparáveis ao cuidado presencial em termos de perda de peso. No entanto, aplicativos móveis isolados, sem componente de acompanhamento clínico, não alcançaram perda de peso clinicamente significativa (>5% do peso corporal).

### 2.2 Componentes Associados à Maior Eficácia

A evidência converge para identificar que os programas digitais mais eficazes para obesidade compartilham determinados componentes ativos (JMIR mHealth uHealth, 2025; PubMed 40829125):

1. **Automonitoramento estruturado** — registro alimentar, de peso e de atividade física
2. **Feedback personalizado** — algoritmos ou profissionais que respondem aos dados registrados
3. **Suporte clínico humano** — reduz a dependência exclusiva de automação
4. **Metas progressivas e adaptativas** — ajustadas ao progresso individual
5. **Elementos de teoria comportamental** — autoeficácia, resolução de problemas, prevenção de recaídas
6. **Frequência de contato** — programas com check-ins semanais superam os mensais

### 2.3 Limitações Reconhecidas

As mesmas meta-análises documentam limitações importantes: alta heterogeneidade estatística (I² > 75% em vários desfechos), viés de seleção (participantes de estudos tendem a ser mais motivados), e perda de seguimento elevada (attrition). O campo caminha para reconhecer que intervenções puramente digitais sem suporte clínico têm eficácia limitada a longo prazo — argumento a favor de modelos híbridos como o proposto pela plataforma de monitoramento metabólico.

---

## 3. Medicina Comportamental e Adesão

### 3.1 Adesão como Variável Central nos Desfechos

A adesão é reconhecida como o fator determinante do benefício clínico em intervenções de perda de peso. Uma umbrella review publicada na Obesity Reviews em 2024 (Wang et al., DOI: 10.1111/obr.13783) analisou os fatores que influenciam a adesão em populações com sobrepeso e obesidade, concluindo que:

- O automonitoramento demonstrou ser eficaz em intervenções comportamentais, dietéticas e multicomponentes
- A tecnologia mostrou potencial particularmente em intervenções dietéticas, comportamentais e multicomponentes
- Intervenções multicomponentes são estratégias promotoras de adesão por excelência, embora necessitem de mais evidências para intervenções farmacológicas

### 3.2 Impacto da Frequência de Check-ins

As diretrizes clínicas para tratamento de obesidade recomendam consistentemente monitoramento frequente como componente essencial da gestão terapêutica:

**Frequência recomendada:**
- Avaliação de eficácia e segurança: ao menos mensalmente nos primeiros 3 meses (AHA Scientific Statement, Circulation, 2023)
- Seguimento subsequente: ao menos a cada 3 meses
- Reforço da adesão comportamental: em cada revisão clínica

A implementação de check-ins regulares mediados por tecnologia digital tem demonstrado resultados comparáveis ao acompanhamento presencial frequente, com vantagens logísticas evidentes para pacientes com barreiras de acesso ao cuidado (Endocrine Society Guidelines, 2024).

### 3.3 Modelos Teóricos Aplicados

Os programas digitais mais eficazes incorporam princípios das seguintes teorias comportamentais validadas:

**Teoria Social Cognitiva (Bandura):** Autoeficácia percebida e modelagem de comportamento mediadas por feedback contínuo sobre progresso — diretamente implementável via dashboards de pontuação metabólica.

**Modelo Transteórico de Mudança (Prochaska & DiClemente):** Estágios de prontidão para mudança guiam a personalização do conteúdo e das intervenções digitais.

**Teoria da Autodeterminação (Ryan & Deci):** Autonomia, competência e vínculo como necessidades psicológicas básicas — atendidas por plataformas que empoderam o paciente com dados compreensíveis sobre seu próprio estado de saúde.

**Terapia Cognitivo-Comportamental (CBT):** Diretrizes americanas de cardiologia (AHA, 2023) e endocrinologia reconhecem a CBT como componente eficaz do tratamento da obesidade, passível de entrega parcial por plataformas digitais estruturadas.

### 3.4 Self-Monitoring Digital: Evidência Quantificada

Um protocolo de ensaio clínico fatorial registrado no JMIR Research Protocols (2025) — "Optimizing Self-Monitoring in a Digital Weight Loss Intervention (Spark)" — representa o estado da arte da investigação sobre automonitoramento digital, reconhecendo que a frequência e o tipo de automonitoramento são variáveis manipuláveis com impacto mensurável nos desfechos. Este ensaio está em andamento com publicação de resultados primários esperada para 2026.

---

## 4. Sistemas de Pontuação de Saúde Metabólica

### 4.1 Limitações das Definições Dicotômicas

A síndrome metabólica (MetS) tem sido historicamente definida de forma dicotômica — presente ou ausente — com critérios do IDF, NCEP ATP III e da harmonização de 2009. Embora clinicamente úteis para diagnóstico, essas definições binárias apresentam limitações substanciais:

- Perdem informação sobre a gravidade e a trajetória temporal da síndrome
- Não capturam estados subclínicos de disfunção metabólica
- Não são sensíveis a pequenas mudanças clinicamente relevantes
- Dificultam a comparação longitudinal do mesmo paciente

A necessidade de escores contínuos foi reconhecida pela comunidade científica, resultando no desenvolvimento de múltiplos sistemas alternativos.

### 4.2 MetS Z-Score (cMetS)

O escore de síndrome metabólica baseado em z-scores (cMetS) representa a abordagem estatística mais rigorosa para quantificação contínua da síndrome metabólica. Cada componente é expresso como desvio padronizado em relação à média de uma população de referência, e o escore composto captura a magnitude total da disfunção.

Um estudo de validação publicado em 2023 em adolescentes espanhóis (MDPI J Personalized Medicine, PMC9865991) demonstrou que o cMetS baseado em z-scores apresentou a maior área sob a curva ROC (AUC = 0,81; IC 95%: 0,784–0,838) para discriminação de síndrome metabólica, com especificidade de 64,4%. A conclusão foi que o cMetS é o método mais acurado para uso em pesquisa, embora seja mais complexo para aplicação clínica rotineira.

### 4.3 siMS Score (Simple Metabolic Score)

O siMS Score foi desenvolvido por Soldatovic et al. (PLOS One, 2016; PMC4706421) como método simples para quantificação contínua da síndrome metabólica em contexto clínico:

```
siMS = 2 × (Cintura/Altura) + Glicemia/5,6 + Triglicerídeos/1,7 + PA_sistólica/130 − HDL/1,02 (homens)
siMS = 2 × (Cintura/Altura) + Glicemia/5,6 + Triglicerídeos/1,7 + PA_sistólica/130 − HDL/1,28 (mulheres)
```

Validações subsequentes (PubMed 30672711; PMC9845596) confirmaram que o siMS é útil para quantificar a gravidade cardiometabólica em indivíduos que não preenchem critérios diagnósticos completos para síndrome metabólica — precisamente o grupo de maior relevância para intervenção preventiva precoce.

### 4.4 CMDS (Cardiometabolic Disease Staging)

O sistema CMDS estratifica o risco cardiometabólico em cinco estágios (0–4) baseados na presença e gravidade de fatores de risco, permitindo identificar pacientes em diferentes pontos do espectro de disfunção metabólica e direcionar a intensidade da intervenção.

### 4.5 Escore de Severidade da Síndrome Metabólica (MetS-SS)

O MetS-SS, desenvolvido e validado nos estudos Atherosclerosis Risk in Communities (ARIC) e Jackson Heart Study (Diabetology & Metabolic Syndrome, 2018), demonstrou capacidade preditiva incremental para doença cardiovascular incidente e diabetes tipo 2 além dos fatores de risco tradicionais, validando a abordagem de escore contínuo para estratificação de risco longitudinal.

### 4.6 Posicionamento do SMI em Relação aos Sistemas Existentes

O Score Metabólico Integrado (SMI) proposto nesta plataforma se diferencia dos sistemas acima pelos seguintes aspectos:

| Característica | cMetS | siMS | CMDS | MetS-SS | **SMI** |
|----------------|-------|------|------|---------|---------|
| Contínuo | Sim | Sim | Não | Sim | **Sim** |
| Multidomínio além de MetS clássico | Não | Não | Não | Não | **Sim** |
| Inclui inflamação | Não | Não | Parcial | Não | **Sim** |
| Inclui eixo hormonal | Não | Não | Não | Não | **Sim** |
| Inclui micronutrientes | Não | Não | Não | Não | **Sim** |
| Desenhado para monitoramento longitudinal | Parcial | Sim | Não | Parcial | **Sim** |
| Aplicável via plataforma digital | Parcial | Sim | Sim | Parcial | **Sim** |

O SMI representa uma evolução dos sistemas existentes ao incorporar domínios biologicamente relevantes que os escores clássicos ignoram — especificamente o eixo hormonal e os micronutrientes — e ao ser desenhado desde o início para uso em plataforma de monitoramento digital longitudinal.

---

## 5. Inteligência Artificial em Suporte à Decisão Clínica

### 5.1 Posicionamento Atual da IA na Medicina Metabólica

A Obesity Medicine Association (OMA) publicou em 2023 uma Clinical Practice Statement dedicada à inteligência artificial no manejo da obesidade (PubMed 37990659), reconhecendo que a IA "está contribuindo para uma evolução e revolução no cuidado médico, incluindo o manejo de pacientes com obesidade." O documento posiciona a IA como ferramenta de suporte — não substituição — do julgamento clínico.

Uma revisão abrangente publicada na PMC em 2025 (PMC11816645) confirma que ferramentas de IA são essenciais para o monitoramento de índices como pressão arterial e glicose, e para a identificação de tendências que orientam ajustes terapêuticos.

### 5.2 Acurácia de Modelos de IA em Desfechos Metabólicos

Estudos recentes documentam a acurácia de modelos de aprendizado de máquina aplicados à saúde metabólica:

- **Random Forest** para predição de obesidade: 86,5% de acurácia (Frontiers in Physiology, 2025; PMC12308079)
- **Gradient Boosting** em predição de síndrome metabólica: AUC > 0,85 em múltiplos estudos
- **Modelos multimodais** (antropométricos + bioquímicos + clínicos): consistentemente superam modelos unimodais
- **Large Language Models (LLMs)** em contexto clínico: demonstram capacidade de síntese de dados complexos com qualidade comparável a especialistas em tarefas estruturadas (Frontiers in Medicine, 2025; DOI: 10.3389/fmed.2025.1698366)

### 5.3 IA para Resumos Clínicos Automatizados

A literatura recente sobre modelos de linguagem em medicina destaca a capacidade de LLMs para síntese de dados clínicos de múltiplas fontes em formatos compreensíveis para médicos e pacientes. A "inteligência colaborativa" — combinação de expertise humana com capacidade analítica da IA — é citada como o paradigma mais seguro e eficaz (Frontiers in Medicine, 2025).

**Requisitos de segurança identificados pela literatura:**
1. Transparência e explicabilidade (XAI — Explainable AI)
2. Validação em populações diversas para mitigar viés
3. Supervisão clínica humana obrigatória nas decisões de alto impacto
4. Auditorias periódicas de desempenho do modelo

### 5.4 Análise de Tendências por IA em Dados Longitudinais

A capacidade da IA de identificar padrões em séries temporais de dados metabólicos — detectando deteriorações subclínicas antes que se tornem clinicamente manifestas — representa uma das aplicações de maior valor clínico e econômico. O Egyptian Journal of Internal Medicine (2024) documenta revisão abrangente do papel da IA na prevenção e gestão da síndrome metabólica, confirmando a viabilidade desta abordagem.

---

## 6. OCR para Resultados Laboratoriais

### 6.1 Estado da Arte da Tecnologia OCR em Saúde

O reconhecimento óptico de caracteres (OCR) em contexto clínico evoluiu substancialmente com a integração de redes neurais profundas e modelos de linguagem. As aplicações em saúde abrangem captura de sinais vitais, prescrições, prontuários externos e resultados laboratoriais.

### 6.2 Evidências de Acurácia

**Estudo multicêntrico prospectivo (Critical Care, 2025; PMC11917072):**
Conduzido em UTIs de Hong Kong, Tailândia e Austrália entre abril de 2023 e fevereiro de 2024, o estudo validou um sistema de entrada de dados baseado em OCR. Em validação independente por 8 profissionais não treinados envolvendo 1.018 pontos de dados:

- Completude global dos dados: **98,5%** (variação: 98,2–100%)
- O sistema demonstrou eficácia e eficiência na facilitação de entrada de dados em bancos de dados clínicos

**Dados históricos de referência:**
Um sistema clínico avaliado em cenário real demonstrou taxa de reconhecimento de dígitos de **92,4%** (IC 95%: 91,6–93,2), com velocidade aproximadamente três vezes superior à entrada manual de dados (PMC2244242).

**Aplicação em prontuários externos (Mayo Clinic Proceedings: Digital Health, 2024; S2949-7612(24)00075-0):**
A Mayo Clinic relatou experiência positiva com sistema de busca baseado em OCR para revisão de prontuários externos, demonstrando viabilidade clínica em ambiente de alta complexidade.

### 6.3 Desafios e Melhores Práticas

A literatura identifica os seguintes desafios e suas soluções:

| Desafio | Solução Recomendada |
|---------|---------------------|
| Variabilidade de layouts de laudos | Treinamento com corpus diversificado de laudos brasileiros |
| Reconhecimento de escrita manual | Híbrido OCR + NLP para normalização |
| Abreviaturas e termos laboratoriais | Dicionário controlado de unidades e nomes de exames |
| Validação dos valores extraídos | Verificação por intervalos de referência com alerta de anomalias |
| Privacidade dos dados de imagem | Processamento local (on-device) ou criptografia ponta a ponta |

A combinação de OCR com processamento de linguagem natural (NLP) para automação de pesquisa clínica foi documentada como abordagem eficaz (PubMed 35608136), resultando em extração estruturada de dados laboratoriais com mínima intervenção humana.

---

## 7. Engajamento do Paciente via Dashboards

### 7.1 Evidências do Impacto de Dashboards em Desfechos

Uma revisão sistemática publicada em 2025 (PMC12296400) examinou o impacto clínico e econômico de dashboards digitais no cuidado hospitalar. Em 20 achados sobre mortalidade (16 estudos), cinco reportaram redução, reforçando que os dashboards não são neutros — seu design e contexto de implementação determinam o impacto.

Uma revisão separada sobre dashboards interativos como ferramentas de feedback e auditoria em atenção primária (PMC12204514, 2025) identificou que estratégias de implementação pareadas com dashboards — incluindo educação, engagement de stakeholders e integração com prontuário eletrônico — são essenciais para que os dashboards se traduzam em mudança de comportamento clínico.

### 7.2 Visualização de Progresso e Motivação

A literatura de psicologia comportamental e medicina digital confirma que a visualização de progresso ativa mecanismos motivacionais baseados em:

- **Efeito de proximidade à meta (goal gradient effect):** Conforme o indivíduo vê seu progresso aproximar-se da meta, a motivação e a frequência do comportamento aumentam (Huang & Aaker, 2019)
- **Reciprocidade de dados:** Pacientes que recebem feedback sobre seus próprios dados demonstram maior engajamento e sensação de controle sobre sua saúde (HIMSS, 2024)
- **Redução de hospitalização:** Estudo de 2023 indicou redução de 25% em readmissões hospitalares para pacientes com doenças crônicas usando soluções de monitoramento remoto com visualização de dados (HealthcareITNews, 2025)

### 7.3 Requisitos para Dashboards Eficazes em Saúde Metabólica

Uma scoping review publicada na PMC (PMC11651422, 2024) sobre métodos de desenvolvimento, implementação e avaliação de dashboards em saúde estabelece os seguintes requisitos para eficácia:

1. **Indicadores-chave de desempenho baseados em evidências** — não todos os dados disponíveis, apenas os clinicamente relevantes
2. **Acessibilidade para o usuário final** — design centrado no paciente, não no clínico
3. **Feedback acionável** — o dashboard deve sugerir próximos passos, não apenas mostrar dados
4. **Contextualização temporal** — comparação com histórico do próprio paciente, não apenas com referências populacionais
5. **Integração com fluxo de cuidado** — alertas automáticos para a equipe clínica quando indicadores críticos são identificados

---

## 8. Programas Digitais de Medicina do Estilo de Vida

### 8.1 Virta Health

A Virta Health é o programa digital de medicina do estilo de vida com o maior corpo de evidências publicadas em periódicos revisados por pares, focando em reversão de diabetes tipo 2 via terapia nutricional com restrição de carboidratos e cetose nutricional, com suporte médico remoto contínuo.

**Desfechos publicados:**

| Horizonte | HbA1c | Peso Corporal | Reversão do DM2 |
|-----------|-------|---------------|-----------------|
| 1 ano (Hallberg et al., 2018; PMC6104272) | −7,6% (6,3% vs. 7,6% basal) | −12% | 60% dos elegíveis |
| 2 anos (Virta Blog, 2019) | ~−2× vs. comparadores | Sustentado | 55% dos completadores |
| 5 anos (Diabetes Research & Clinical Practice, 2024) | −0,3% (sustentado) | −7,6% (sustentado) | 32,5% (HbA1c < 6,5% sem medicação ou só metformina) |

Os dados de 5 anos (DOI disponível em Diabetes Research & Clinical Practice, 2024) demonstram sustentabilidade dos benefícios em subconjunto de participantes que mantiveram engajamento com o programa — o que é relevante ao apontar que retenção e adesão são os principais moderadores de desfecho.

### 8.2 Noom

A Noom é o maior programa digital de gestão de peso em atividade, com mais de 50 milhões de membros. Baseia-se em psicologia comportamental e coaching digital. Estudos indicam taxas de reversão de diabetes superiores a grupos-controle, embora a qualidade metodológica dos estudos seja variável (NCBI Bookshelf, Evidence Brief).

**Componente diferencial:** Utiliza psicologia cognitivo-comportamental integrada ao design do aplicativo, com coaching humano em momentos-chave da jornada do paciente.

### 8.3 Lark Health

A Lark Health é uma plataforma de coaching digital para diabetes e pré-diabetes, reconhecida pelo CDC dos EUA como programa de prevenção de diabetes. Utiliza chatbot baseado em IA para fornecer coaching contínuo, com estudos demonstrando redução de HbA1c e melhora em marcadores metabólicos em populações com pré-diabetes.

### 8.4 Livongo (Teladoc Health)

A plataforma Livongo foi pioneira no conceito de "Applied Health Signals" — combinação de dispositivos conectados, dados comportamentais e coaching preditivo. Seus dados clínicos mostram melhorias em controle glicêmico, pressão arterial e engajamento do paciente. O PHTI (Peterson Health Technology Institute) incluiu Livongo entre as plataformas avaliadas em 2024, com resultados mistos sobre custo-efetividade (FierceHealthcare, 2024).

### 8.5 Lições Aprendidas e Implicações Competitivas

A análise comparativa desses programas revela padrões consistentes:

- **Programas com suporte clínico humano** (Virta) superam significativamente programas puramente automatizados em desfechos clínicos distal
- **Programas com monitoring contínuo** apresentam melhor retenção e desfechos superiores a programas baseados em consultas episódicas
- **Questionamentos sobre custo-efetividade** (PHTI, 2024) não se dirigem ao modelo clínico, mas ao modelo de remuneração — reforçando a necessidade de demonstrar valor por meio de desfechos quantificados
- **Nenhum programa combina** monitoramento metabólico multidomínio, OCR de laudos, pontuação integrada e suporte clínico num único produto voltado ao mercado brasileiro

---

## 9. Marco Regulatório Brasileiro

### 9.1 Lei Geral de Proteção de Dados (LGPD) — Artigo 11

A LGPD (Lei nº 13.709/2018) estabelece o regime jurídico de proteção de dados pessoais no Brasil. O **Artigo 11** disciplina especificamente o tratamento de dados pessoais sensíveis — categoria que abrange todos os dados de saúde coletados pela plataforma — incluindo:

**Hipóteses legais para tratamento de dados de saúde (Art. 11):**
- Consentimento do titular de forma específica e destacada (Art. 11, I)
- Tutela da saúde, em procedimento realizado por profissionais de saúde ou autoridades sanitárias (Art. 11, II, f)
- Proteção da vida ou incolumidade física do titular ou de terceiros (Art. 11, II, e)

**Requisitos operacionais:**
- Pseudonimização e anonimização como medidas de proteção preferenciais
- Registro de operações de tratamento (ROPA — Records of Processing Activities)
- Relatório de Impacto à Proteção de Dados Pessoais (RIPD) para tratamento de dados sensíveis
- Nomeação de Encarregado de Dados (DPO — Data Protection Officer)
- Armazenamento local (Brasil) ou garantias equivalentes para transferências internacionais

A LGPD não define prazo de retenção para dados de saúde, remetendo às normas setoriais — no caso de prontuários médicos, o CFM estabelece 20 anos mínimos para prontuários digitais.

### 9.2 Resolução CFM nº 2.314/2022 — Telemedicina

A Resolução CFM nº 2.314/2022, publicada em maio de 2022, estabelece o marco regulatório nacional da telemedicina, definindo-a como "o exercício da medicina mediado por Tecnologias Digitais, de Informação e de Comunicação (TDICs), para fins de assistência, educação, pesquisa, prevenção de doenças e lesões, gestão e promoção de saúde."

**Modalidades regulamentadas aplicáveis à plataforma:**

| Modalidade | Descrição | Aplicabilidade ao Produto |
|------------|-----------|--------------------------|
| Teleconsulta | Atendimento médico síncrono a distância | Check-ins médicos e ajustes de conduta |
| Telemonitoramento | Monitoramento de dados do paciente à distância | Core da plataforma (SMI + alertas) |
| Telerregulação | Regulação de acesso e fluxos assistenciais | Encaminhamentos e escalonamento |
| Telegynecologia/Teleendocrinologia | Especialidades à distância | Suporte especializado |

**Requisitos documentais:**
- Prontuário eletrônico obrigatório para toda teleconsulta (Art. 6º)
- Dados e imagens dos pacientes devem ser preservados seguindo normas legais de guarda, manuseio, integridade, veracidade, confidencialidade, privacidade, irrefutabilidade e garantia do sigilo profissional
- Consentimento informado específico para telemedicina

**Atualização 2024:** A Resolução CFM 2.382/2024 padronizou atestados emitidos por telemedicina, e decisão do TRT-SP em 2024 reconheceu validade plena de atestados telemédicos, consolidando o marco regulatório.

### 9.3 ANVISA e Regulamentação de Software como Dispositivo Médico

A RDC ANVISA nº 657/2022 dispõe sobre requisitos sanitários para Sistemas de Registro Eletrônico em Saúde (S-RES), estabelecendo critérios de segurança, rastreabilidade e certificação aplicáveis a plataformas digitais de saúde.

Plataformas digitais que realizam análise de dados de saúde para suporte à decisão clínica podem ser enquadradas como **Software como Dispositivo Médico (SaMD)** pela ANVISA, conforme a RDC nº 657/2022 e orientações do International Medical Device Regulators Forum (IMDRF). O enquadramento como SaMD impõe:

- Registro ou notificação na ANVISA, dependendo da classe de risco
- Sistema de gerenciamento de qualidade (ISO 13485)
- Documentação de validação clínica e técnica
- Plano de vigilância pós-mercado (Farmacovigilância/Tecnovigilância)

**Estratégia recomendada:** A plataforma deve ser enquadrada como SaMD de baixo risco (Classe I ou II) se posicionada como suporte à decisão clínica — não substituição do julgamento médico. Relatórios gerados pela IA devem ser explicitamente classificados como "informativos" e a decisão clínica final deve recair sobre o profissional de saúde qualificado.

### 9.4 Marco Legal da Telessaúde no Brasil

Além das regulamentações do CFM, o marco legal da telessaúde no Brasil inclui:

- **Lei nº 14.510/2022:** Estabelece diretrizes para prática da telessaúde no Brasil e regula a teleconsulta
- **Portaria GM/MS nº 567/2023:** Regulamenta o Programa Nacional de Telessaúde no âmbito do SUS
- **Resolução CFM nº 2.314/2022** (já descrita): Principal norma deontológica

---

## 10. Score Metabólico Integrado (SMI)

### 10.1 Fundamento Conceitual

O Score Metabólico Integrado (SMI) é um instrumento de pontuação contínua e multidomínio desenhado para capturar a saúde metabólica global do indivíduo de forma holística, longitudinal e sensível a mudanças. Seu desenvolvimento fundamenta-se na crescente evidência de que a saúde metabólica não é redutível a poucos parâmetros clínicos clássicos — glicemia, pressão arterial, lipídios e circunferência abdominal — mas emerge da interação de múltiplos sistemas biológicos interconectados.

O SMI é composto por **seis domínios**, cada um com peso específico derivado da contribuição relativa de cada sistema na determinação do risco metabólico global, conforme documentado na literatura científica:

```
SMI = (Composição Corporal × 0,25) + (Metabolismo Glicêmico × 0,20) +
      (Inflamação Metabólica × 0,15) + (Perfil Lipídico × 0,15) +
      (Eixo Hormonal × 0,15) + (Micronutrientes × 0,10)
```

### 10.2 Domínio 1: Composição Corporal (25%)

**Justificativa científica para o peso de 25%:**

A composição corporal é o domínio com maior peso no SMI por três razões fundamentais:

1. **Determinismo central:** A adiposidade visceral é o principal driver fisiopatológico da síndrome metabólica, causando resistência à insulina, dislipidemia aterogênica, hipertensão e estado pró-inflamatório via secreção de adipocinas disfuncionais (Endotext, NBK279053)

2. **Superioridade preditiva sobre BMI isolado:** A American Medical Association (AMA, 2023) publicou recomendação explícita para que avaliações de saúde incluam medidas de distribuição de gordura além do IMC. O relatório Strengths and Limitations of BMI (PMC11306271, 2024) documenta que o IMC isolado misclassifica 20–30% dos pacientes em termos de risco metabólico real

3. **Validade incremental da circunferência abdominal:** A International Atherosclerosis Society e o International Chair on Cardiometabolic Risk recomendam a circunferência abdominal como medida de rotina clínica (Nature Reviews Endocrinology, 2019). A razão cintura-estatura (RCE) demonstrou as associações mais fortes com desfechos metabólicos adversos em análise comparativa de medidas de adiposidade (medRxiv, 2025)

**Biomarcadores e métricas incluídas no domínio:**
- Índice de Massa Corporal (IMC)
- Circunferência abdominal
- Razão cintura-estatura (RCE)
- Percentual de gordura corporal (quando disponível)
- Massa muscular/índice de massa muscular esquelética

### 10.3 Domínio 2: Metabolismo Glicêmico (20%)

**Justificativa científica para o peso de 20%:**

O metabolismo glicêmico é o segundo domínio mais pesado por representar o elo central entre adiposidade, inflamação, risco cardiovascular e diabetes tipo 2 — a complicação metabólica de maior prevalência e impacto no sistema de saúde.

**Evidências de suporte:**

A revisão PMC4137169 demonstrou que um painel abrangente de biomarcadores glicêmicos, de resistência à insulina e de função de células beta identifica risco diabético em 45% mais pacientes do que a abordagem restrita à glicemia de jejum e HbA1c. Isso fundamenta a incorporação de múltiplos marcadores glicêmicos no SMI, não apenas a glicemia de jejum.

O Standards of Care in Diabetes 2026 (PMC12690183) reafirma que:
- HbA1c permanece o biomarcador padrão de controle glicêmico de médio prazo
- HOMA-IR é o proxy clínico mais utilizado para resistência à insulina
- Glicemia 2h pós-carga (TOTG) identifica disglicemia em pacientes com glicemia de jejum normal

**Biomarcadores incluídos no domínio:**
- Glicemia de jejum
- Hemoglobina glicada (HbA1c)
- Insulina de jejum e HOMA-IR
- Peptídeo C (quando disponível)
- Glicemia pós-prandial (quando disponível)

### 10.4 Domínio 3: Inflamação Metabólica (15%)

**Justificativa científica para o peso de 15%:**

A inflamação crônica de baixo grau é reconhecida como característica fisiopatológica central da obesidade e da síndrome metabólica — não apenas uma consequência, mas um mecanismo ativo de perpetuação e progressão da disfunção metabólica.

**Evidências quantificadas:**

- OR para síndrome metabólica com CRP elevada: **1,89** (Nutrition & Metabolism, Springer)
- OR para síndrome metabólica com IL-6 elevada: **2,11** (mesma revisão)
- A PCR-us demonstrou efeito mais estável e reprodutível que outros marcadores inflamatórios, sendo adequada para uso clínico (MDPI IJMS, 2024; 11540)
- Mesmo em obesos "metabolicamente saudáveis" (MHO), níveis de PCR-us significativamente elevados versus não-obesos saudáveis indicam que a inflamação subclínica precede manifestações clínicas da síndrome metabólica (Nature EJCN, 2011; validado por múltiplos estudos subsequentes)

**Biomarcadores incluídos no domínio:**
- Proteína C-Reativa ultrassensível (PCR-us)
- Interleucina-6 (IL-6) — quando disponível
- Velocidade de hemossedimentação (VHS)
- Ferritina sérica (marcador inflamatório e de reservas de ferro)
- Ácido úrico (marcador de inflamação e resistência à insulina)

### 10.5 Domínio 4: Perfil Lipídico (15%)

**Justificativa científica para o peso de 15%:**

O perfil lipídico aterogênico — elevação de triglicerídeos, redução de HDL-C e predominância de partículas LDL pequenas e densas — é componente essencial da síndrome metabólica e preditor independente de doença cardiovascular.

**Evidências de suporte:**

A razão TG/HDL-C emergiu como biomarcador de relevância crescente:
- Alta razão TG/HDL-C foi observada em 72,2% dos sujeitos com síndrome metabólica
- Associação significativa com eventos cardiovasculares maiores (OR = 3,32; p = 0,025) (JACL, 2024)
- A razão TG/HDL-C é proxy validado de resistência à insulina e tamanho de partículas LDL

As diretrizes 2025 da American Association of Clinical Endocrinology (Endocrine Practice, 2025) e a AHA/ACC de 2018 fundamentam a inclusão de LDL-C, não-HDL-C, TG e HDL-C como biomarcadores essenciais.

**Biomarcadores incluídos no domínio:**
- Colesterol total
- LDL-C (calculado ou direto)
- HDL-C
- Triglicerídeos
- Não-HDL-C
- Razão TG/HDL-C
- Apoliproteína B (ApoB) — quando disponível

### 10.6 Domínio 5: Eixo Hormonal (15%)

**Justificativa científica para o peso de 15%:**

O eixo hormonal representa domínio único do SMI em relação a todos os sistemas de pontuação existentes — e essa inovação é sustentada por sólida base fisiopatológica. A obesidade é tanto causa quanto consequência de disfunções em múltiplos eixos endócrinos, criando ciclos viciosos que perpetuam a disfunção metabólica.

**Evidências por subdomínio:**

**Eixo tireoidiano:**
Os hormônios tireoidianos (T3 e T4) regulam a taxa metabólica basal, o metabolismo lipídico e a homeostase glicêmica. Hipotireoidismo subclínico é encontrado com frequência aumentada em obesidade e contribui para resistência à perda de peso (Endotext, NBK279053).

**Eixo hipotálamo-hipófise-adrenal (cortisol):**
O cortisol promove gliconeogênese e lipólise, mas cronicamente elevado causa resistência à insulina, obesidade central e dislipidemia. O estresse crônico como modulador metabólico é fisiopatologicamente central e clinicamente negligenciado (Longdom Endocrinology, 2025).

**Eixo hipotálamo-hipófise-gonadal:**
Em obesidade masculina, hipoandrogenismo (redução de testosterona livre) é prevalente e bidirecional — baixa testosterona causa aumento de gordura visceral e resistência à insulina, que por sua vez suprimem a produção de testosterona (Springer Journal of Evolutionary Biochemistry, 2025). Em mulheres, a síndrome dos ovários policísticos (SOP) representa a manifestação endócrino-metabólica mais comum.

**Adipocinas:**
A leptina e a adiponectina são hormônios produzidos pelo tecido adiposo que modulam diretamente a sensibilidade à insulina e o estado inflamatório. Na obesidade:
- Leptina: elevada, com resistência ao seu efeito (leptinorresistência)
- Adiponectina: reduzida, associada a resistência à insulina, dislipidemia e aterosclerose (Wiley MNF&R, 2025; PMC11857386)

**Biomarcadores incluídos no domínio:**
- TSH, T3 livre, T4 livre
- Cortisol matinal (ou perfil circadiano quando disponível)
- Testosterona total e livre (homens)
- SHBG (Sex Hormone-Binding Globulin)
- Estradiol (mulheres na pós-menopausa)
- Adiponectina e leptina (quando disponíveis)
- GH e IGF-1 (quando indicado)

### 10.7 Domínio 6: Micronutrientes (10%)

**Justificativa científica para o peso de 10%:**

Embora com peso menor que os demais domínios, os micronutrientes representam uma camada clinicamente relevante e frequentemente negligenciada na avaliação metabólica. A obesidade per se é um estado de risco aumentado para deficiências de micronutrientes — paradoxo bem documentado da "desnutrição no excesso" (Tandfonline, 2024; DOI: 10.1080/09540105.2024.2381725).

**Evidências de prevalência:**

Indivíduos com obesidade apresentam taxas elevadas de deficiências de:
- Vitamina D (frequentemente abaixo de 20 ng/mL)
- Magnésio (envolvido em mais de 300 reações enzimáticas do metabolismo de carboidratos e lipídios)
- Zinco (cofator de mais de 300 enzimas, envolvido no metabolismo de carboidratos e gorduras)
- Vitamina B12
- Folato
- Ferro e ferritina

**Relevância metabólica:**

- A deficiência de vitamina D está associada a resistência à insulina, síndrome metabólica e pior controle glicêmico
- A deficiência de magnésio prejudica a ativação da vitamina D e reduz sua eficácia anti-inflamatória (Frontiers in Nutrition, 2025; PMC sobre magnesium-vitamin D interaction)
- A deficiência de zinco compromete a sinalização de insulina e a resposta imune metabólica
- A revisão ESPEN 2023 (ScienceDirect, 2023) documentou que micronutrientes têm relevância direta na prática clínica, justificando sua inclusão em avaliações metabólicas abrangentes

**Biomarcadores incluídos no domínio:**
- 25-OH-Vitamina D
- Magnésio sérico
- Zinco sérico
- Vitamina B12
- Ferritina sérica (compartilhada com domínio de inflamação com peso diferenciado)
- Folato
- Selênio (quando disponível)

### 10.8 Validação Psicométrica e Calibração do SMI

Para que o SMI seja cientificamente válido, seu desenvolvimento deve seguir o processo de validação de instrumentos composto:

1. **Validade de conteúdo:** Revisão por painel Delphi de especialistas em endocrinologia, medicina do estilo de vida e medicina metabólica (Rodada 1: consenso sobre domínios; Rodada 2: consenso sobre pesos)

2. **Validade de construto:** Análise fatorial confirmatória em coorte de desenvolvimento com dados laboratoriais completos (n ≥ 500)

3. **Validade de critério concorrente:** Correlação do SMI com desfechos clínicos estabelecidos (diagnóstico de síndrome metabólica, HOMA-IR, Framingham Risk Score)

4. **Validade preditiva:** Capacidade do SMI de prever eventos metabólicos incidentes em seguimento prospectivo

5. **Responsividade:** Sensibilidade à mudança clínica relevante em intervenções de perda de peso e modificação do estilo de vida

6. **Confiabilidade:** Consistência interna (Cronbach's alpha ≥ 0,70) e reprodutibilidade teste-reteste

Este processo de validação é requisito ético e científico antes de qualquer uso do SMI para guiar decisões clínicas, e deve ser planejado como componente do roadmap de pesquisa da plataforma.

---

## 11. Implicações para o Produto

### 11.1 Validação da Proposta de Valor Central

A literatura revisada valida com nível de evidência moderado a alto os seguintes componentes da proposta de valor da plataforma:

| Componente do Produto | Suporte Científico | Nível de Evidência |
|-----------------------|--------------------|--------------------|
| Monitoramento remoto entre consultas (RTM) | CMS, APTA, npj Digital Medicine 2024 | Moderado-Alto |
| Score contínuo de saúde metabólica (SMI) | cMetS, siMS, MetS-SS literature | Moderado |
| OCR de laudos laboratoriais | Critical Care 2025, Mayo Clinic Digital Health | Moderado |
| Dashboard de progresso para paciente | PMC12296400, HIMSS 2024 | Moderado |
| Alertas clínicos baseados em IA | OMA CPS 2023, Frontiers Medicine 2025 | Emergente |
| Suporte comportamental digital | Obesity Reviews 2024, JMIR 2025 | Alto |
| Resumos clínicos automatizados por IA | OMA CPS 2023, Egyptian J Internal Medicine 2024 | Emergente |

### 11.2 Diferenciação Competitiva Sustentada por Evidência

A análise dos programas comparáveis (Seção 8) confirma que nenhum competidor identificado combina:

1. **Pontuação metabólica multidomínio** que inclui eixo hormonal e micronutrientes
2. **OCR integrado** para captura automatizada de laudos
3. **Foco no mercado brasileiro** com conformidade com CFM 2.314/2022 e LGPD
4. **Suporte clínico humano** integrado com automação de IA

Esta combinação constitui o espaço de diferenciação defensável da plataforma.

### 11.3 Riscos Científicos Identificados e Mitigações

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| SMI sem validação prospectiva | Alta | Alto | Protocolo de estudo de validação como milestone obrigatório |
| Acurácia do OCR insuficiente para laudos brasileiros | Média | Alto | Dataset de treinamento com laudos do mercado nacional |
| Heterogeneidade de formatos de laudo | Alta | Médio | Parceria com laboratórios para padronização progressiva |
| Obsolescência regulatória (CFM/ANVISA) | Baixa | Alto | Monitoramento contínuo de normas e flexibilidade arquitetural |
| Custo-efetividade não demonstrado | Média | Alto | Coleta prospectiva de dados econômicos desde o lançamento |

### 11.4 Recomendações para o Roadmap de Pesquisa

Com base na revisão científica realizada, as seguintes iniciativas de pesquisa são recomendadas para fortalecer a base evidencial do produto:

1. **Estudo de Validação do SMI** (Fase 1, Meses 6–18): Estudo observacional transversal em coorte de 300–500 pacientes com dados laboratoriais completos, para validação de conteúdo, construto e critério do SMI. Protocolo a ser registrado no ClinicalTrials.gov antes do início.

2. **Estudo de Usabilidade** (Fase 1, Meses 3–9): Avaliação da acurácia do módulo OCR em amostra representativa de laudos brasileiros (n ≥ 1.000 laudos de pelo menos 10 laboratórios diferentes).

3. **Ensaio Clínico Piloto** (Fase 2, Meses 12–24): RCT piloto (n = 100–200) comparando plataforma digital de monitoramento metabólico versus cuidado padrão em pacientes com obesidade e pelo menos um componente de síndrome metabólica. Desfechos primários: SMI aos 6 meses, HbA1c, peso corporal. Desfechos secundários: adesão, satisfação, qualidade de vida, custos.

4. **Publicação Científica** (Fase 2): Publicação dos resultados de validação do SMI e do ensaio piloto em periódico de alto impacto (JMIR, Obesity Reviews, Lancet Digital Health).

### 11.5 Posicionamento Regulatório Recomendado

Com base na análise do marco regulatório brasileiro (Seção 9), recomenda-se:

- **Não enquadrar** a plataforma como dispositivo médico diagnóstico de alto risco (evita registro ANVISA de Classe III/IV)
- **Enquadrar** como SaMD de suporte à decisão clínica de baixo risco (Classe I ou II), com linguagem que deixe clara a natureza informativa — não prescritiva — dos outputs da IA
- **Registrar** o sistema como Plataforma de Telessaúde sob CFM 2.314/2022 e Lei nº 14.510/2022
- **Implementar** conformidade LGPD desde o MVP, com RIPD documentado, DPO nomeado e consentimento granular

---

## 12. Referências

### Regulamentação e Política

1. Centers for Medicare & Medicaid Services (CMS). *Remote Therapeutic Monitoring: Final Rule 2022*. Baltimore: CMS; 2022.

2. American Physical Therapy Association (APTA). *Practice Advisory: Remote Therapeutic Monitoring Codes Under Medicare*. Alexandria: APTA; March 2023. Available at: https://www.apta.org/contentassets/95321a10e951408db650e2f19b96699f/apta-practice-advisory-rtm-codes032023.pdf

3. Conselho Federal de Medicina (CFM). *Resolução CFM nº 2.314/2022 — Telemedicina*. Brasília: CFM; 2022. Available at: https://sistemas.cfm.org.br/normas/arquivos/resolucoes/BR/2022/2314_2022.pdf

4. Brasil. *Lei Geral de Proteção de Dados Pessoais (LGPD) — Lei nº 13.709/2018*. Brasília; 2018.

5. Brasil. *Lei nº 14.510/2022 — Telessaúde*. Brasília; 2022.

6. Tenovi. *Remote Therapeutic Monitoring Codes for 2024 & How to Bill*. 2024. Available at: https://www.tenovi.com/remote-therapeutic-monitoring-codes/

7. ThoroughCare. *2025 Remote Therapeutic Monitoring CPT Codes*. 2025. Available at: https://www.thoroughcare.net/blog/2025-remote-therapeutic-monitoring-cpt-codes

### Remote Therapeutic Monitoring e Monitoramento Remoto

8. Michaud K, et al. *Remote Therapeutic Monitoring in Rheumatic and Musculoskeletal Diseases: Opportunities and Implementation*. PMC10972608. 2024.

9. Mahtani KR, et al. *A systematic review of the impacts of remote patient monitoring (RPM) interventions on safety, adherence, quality-of-life and cost-related outcomes*. npj Digital Medicine. 2024. Available at: https://www.nature.com/articles/s41746-024-01182-w

10. JMIR. *The State of Remote Patient Monitoring for Chronic Disease Management in the United States*. J Med Internet Res. 2025;27:e70422. Available at: https://www.jmir.org/2025/1/e70422

### Intervenções Digitais para Obesidade

11. MDPI Nutrients. *E-Health and M-Health in Obesity Management: A Systematic Review and Meta-Analysis of RCTs*. Nutrients. 2025;17(13):2200. Available at: https://www.mdpi.com/2072-6643/17/13/2200

12. JMIR. *Evaluation of the Aspects of Digital Interventions That Successfully Support Weight Loss: Systematic Review With Component Network Meta-Analysis*. J Med Internet Res. 2025;27:e65443. PMC12141966. Available at: https://www.jmir.org/2025/1/e65443

13. PMC10482795. *The Effectiveness of eHealth Interventions for Weight Loss and Weight Loss Maintenance in Adults with Overweight or Obesity: A Systematic Review of Systematic Reviews*. 2023. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC10482795/

14. JMIR mHealth uHealth. *Behavior Change Resources Used in Mobile App–Based Interventions Addressing Weight, Behavioral, and Metabolic Outcomes in Adults With Overweight and Obesity: Systematic Review and Meta-Analysis of Randomized Controlled Trials*. 2025. PubMed 40829125. Available at: https://mhealth.jmir.org/2025/1/e63313

15. International Journal of Obesity. *The effectiveness and usability of online, group-based interventions for people with severe obesity: a systematic review and meta-analysis*. 2024. Available at: https://www.nature.com/articles/s41366-024-01669-2

### Adesão e Medicina Comportamental

16. Wang Y, et al. *Exploring factors of adherence to weight loss interventions in population with overweight/obesity: an umbrella review*. Obesity Reviews. 2024. DOI: 10.1111/obr.13783. Available at: https://onlinelibrary.wiley.com/doi/10.1111/obr.13783

17. American Heart Association. *Implementation of Obesity Science Into Clinical Practice: A Scientific Statement From the American Heart Association*. Circulation. 2023. Available at: https://www.ahajournals.org/doi/10.1161/CIR.0000000000001221

18. JMIR Research Protocols. *Optimizing Self-Monitoring in a Digital Weight Loss Intervention (Spark): Protocol for a Factorial Randomized Trial*. 2025. Available at: https://www.researchprotocols.org/2025/1/e75629

### Sistemas de Pontuação Metabólica

19. Fernández-Aparicio A, et al. *cMetS Based on Z-Scores as an Accurate and Efficient Scoring System to Determine Metabolic Syndrome in Spanish Adolescents*. J Pers Med. 2023;13(1):10. PMC9865991. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC9865991/

20. Soldatovic I, et al. *siMS Score: Simple Method for Quantifying Metabolic Syndrome*. PLOS One. 2016. PMC4706421. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC4706421/

21. Soldatovic I, et al. *siMS score — method for quantification of metabolic syndrome, confirms co-founding factors of metabolic syndrome*. PMC9845596. 2023. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC9845596/

22. Gurka MJ, et al. *Assessing the added predictive ability of a metabolic syndrome severity score in predicting incident cardiovascular disease and type 2 diabetes: the Atherosclerosis Risk in Communities Study and Jackson Heart Study*. Diabetol Metab Syndr. 2018. Available at: https://dmsjournal.biomedcentral.com/articles/10.1186/s13098-018-0344-3

### Inteligência Artificial em Saúde Metabólica

23. Obesity Medicine Association (OMA). *Artificial intelligence and obesity management: An OMA Clinical Practice Statement (CPS) 2023*. PubMed 37990659. Available at: https://pubmed.ncbi.nlm.nih.gov/37990659/

24. PMC11816645. *Harnessing Artificial Intelligence in Obesity Research and Management: A Comprehensive Review*. 2025. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC11816645/

25. PMC11857386. *The Role of Artificial Intelligence in Obesity Risk Prediction and Management: Approaches, Insights, and Recommendations*. 2025. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC11857386/

26. Frontiers in Medicine. *Trends in AI-based diagnosis and intervention of metabolic diseases: a bibliometric analysis of the literature from 2000 to 2024*. 2025. DOI: 10.3389/fmed.2025.1698366.

27. PMC12308079. *Prediction of obesity levels based on physical activity and eating habits with a machine learning model integrated with explainable artificial intelligence*. 2025. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC12308079/

28. Egyptian Journal of Internal Medicine. *From prevention to management: exploring AI's role in metabolic syndrome management: a comprehensive review*. 2024. Available at: https://ejim.springeropen.com/articles/10.1186/s43162-024-00373-x

### OCR em Saúde

29. PMC11917072. *Streamlining data recording through optical character recognition: a prospective multi-center study in intensive care units*. Critical Care. 2025. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC11917072/

30. Mayo Clinic Proceedings: Digital Health. *Experience With an Optical Character Recognition Search Application for Review of Outside Medical Records*. 2024. Available at: https://www.mcpdigitalhealth.org/article/S2949-7612(24)00075-0/fulltext

31. PubMed 35608136. *Facilitating clinical research through automation: Combining optical character recognition with natural language processing*. 2022.

### Dashboards e Engajamento do Paciente

32. PMC12296400. *Clinical and economic impact of digital dashboards on hospital inpatient care: a systematic review*. 2025. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC12296400/

33. PMC12204514. *Effectiveness of interactive dashboards as audit and feedback tools in primary care: A systematic review*. 2025. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC12204514/

34. PMC11651422. *Development, Implementation, and Evaluation Methods for Dashboards in Health Care: Scoping Review*. 2024. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC11651422/

### Programas Digitais de Medicina do Estilo de Vida

35. Hallberg SJ, et al. *Effectiveness and Safety of a Novel Care Model for the Management of Type 2 Diabetes at 1 Year: An Open-Label, Non-Randomized, Controlled Study*. Diabetes Ther. 2018. PMC6104272. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC6104272/

36. Diabetes Research and Clinical Practice. *5-Year effects of a novel continuous remote care model with carbohydrate-restricted nutrition therapy including nutritional ketosis in type 2 diabetes: An extension study*. 2024. Available at: https://www.diabetesresearchclinicalpractice.com/article/S0168-8227(24)00808-8/fulltext

37. NCBI Bookshelf. *Evidence Brief: Virtual Diet Programs for Diabetes*. Available at: https://www.ncbi.nlm.nih.gov/books/NBK563523/

### Composição Corporal e Adiposidade

38. PMC11306271. *Strengths and Limitations of BMI in the Diagnosis of Obesity: What is the Path Forward?* Curr Obes Rep. 2024. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC11306271/

39. Lean MEJ, et al. *Waist circumference as a vital sign in clinical practice: a Consensus Statement from the IAS and ICCR Working Group on Visceral Obesity*. Nat Rev Endocrinol. 2019. Available at: https://www.nature.com/articles/s41574-019-0310-7

40. medRxiv 2025. *Waist, waist-height-ratio vs body mass index and the risks...* 2025. Available at: https://www.medrxiv.org/content/10.1101/2025.10.16.25338152v1.full.pdf

### Metabolismo Glicêmico

41. PMC4137169. *Comprehensive Biomarker Testing of Glycemia, Insulin Resistance, and Beta Cell Function Has Greater Sensitivity to Detect Diabetes Risk Than Fasting Glucose and HbA1c*. 2014.

42. PMC12690183. *Diagnosis and Classification of Diabetes: Standards of Care in Diabetes — 2026*. 2026. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC12690183/

### Inflamação Metabólica

43. MDPI IJMS. *Systemic Inflammation Across Metabolic Obesity Phenotypes: A Cross-sectional Study of Korean Adults Using High-Sensitivity C-Reactive Protein as a Biomarker*. 2024;25(21):11540. Available at: https://www.mdpi.com/1422-0067/25/21/11540

44. Nutrition & Metabolism (Springer). *Do inflammation and procoagulation biomarkers contribute to the metabolic syndrome cluster?* Available at: https://link.springer.com/article/10.1186/1743-7075-4-28

### Perfil Lipídico

45. MDPI Antioxidants. *HDL-Cholesterol and Triglycerides Dynamics: Essential Players in Metabolic Syndrome*. 2025;14(4):434. Available at: https://www.mdpi.com/2076-3921/14/4/434

46. PMC10001260. *The Triglyceride/High-Density Lipoprotein Cholesterol (TG/HDL-C) Ratio as a Risk Marker for Metabolic Syndrome and Cardiovascular Disease*. 2023. Available at: https://pmc.ncbi.nlm.nih.gov/articles/PMC10001260/

47. Endocrine Practice. *Highlights of the 2025 American Association of Clinical Endocrinology Clinical Practice Guideline on Pharmacologic Management of Adults With Dyslipidemia*. 2025. Available at: https://www.endocrinepractice.org/article/S1530-891X(24)00831-0/fulltext

### Eixo Hormonal

48. Endotext/NCBI Bookshelf. *Endocrine Changes in Obesity*. NBK279053. Available at: https://www.ncbi.nlm.nih.gov/books/NBK279053/

49. Wiley MNF&R. *Obesity, White Adipose Tissue, and Adipokines Signaling in Male Reproduction*. Mol Nutr Food Res. 2025. DOI: 10.1002/mnfr.70054. Available at: https://onlinelibrary.wiley.com/doi/10.1002/mnfr.70054

50. Longdom Endocrinology. *Impact of Hormonal Imbalance on Metabolic Syndrome Progression*. 2025. Available at: https://www.longdom.org/open-access/impact-of-hormonal-imbalance-on-metabolic-syndrome-progression-1101923.html

### Micronutrientes

51. Tandfonline. *Obesity and micronutrients deficit, when and how to supplement*. Food & Nutrition Research. 2024. DOI: 10.1080/09540105.2024.2381725. Available at: https://www.tandfonline.com/doi/full/10.1080/09540105.2024.2381725

52. ScienceDirect. *The science of micronutrients in clinical practice — Report on the ESPEN symposium*. Clinical Nutrition. 2023. Available at: https://www.sciencedirect.com/science/article/pii/S0261561423004284

53. Frontiers in Nutrition. *The effects of magnesium and vitamin D/E co-supplementation on metabolic outcomes*. 2025. DOI: 10.3389/fnut.2025.1563604.

54. SciVision Publishers. *Micronutrients in Metabolic Syndrome: A Comprehensive Review*. Available at: https://www.scivisionpub.com/pdfs/micronutrients-in-metabolic-syndrome-a-comprehensive-review-3863.pdf

---

*Documento elaborado com base em evidências científicas disponíveis até março de 2026. As referências devem ser verificadas individualmente antes de uso em publicações científicas ou documentos regulatórios. Este documento não substitui avaliação clínica individualizada.*

*Versão 1.0 — Pendente de revisão por especialistas clínicos antes de uso definitivo.*
