# Score Metabólico Integrado (SMI) — Regras de Cálculo

## Fórmula
```
SMI = (CC × 0.25) + (MG × 0.20) + (INF × 0.15) + (LIP × 0.15) + (HOR × 0.15) + (MIC × 0.10)
```

Onde cada domínio pontua de 0 a 100.

## Domínio 1 — Composição Corporal (CC) — Peso 25%

| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| IMC | 18.5-24.9 | 25-27.9 | 28-32.9 | ≥33 |
| Circ. abdominal (H) | <80cm | 80-94cm | 94-102cm | >102cm |
| Circ. abdominal (M) | <70cm | 70-80cm | 80-88cm | >88cm |
| % gordura (H) | <15% | 15-20% | 20-28% | >28% |
| % gordura (M) | <22% | 22-28% | 28-35% | >35% |

## Domínio 2 — Metabolismo Glicêmico (MG) — Peso 20%

| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| Glicemia jejum | <90 mg/dL | 90-99 | 100-110 | >110 |
| Insulina | <8 µU/mL | 8-12 | 12-20 | >20 |
| HOMA-IR | <1.5 | 1.5-2.5 | 2.5-3.5 | >3.5 |
| HbA1c | <5.4% | 5.4-5.6% | 5.7-6.2% | >6.2% |

## Domínio 3 — Inflamação Metabólica (INF) — Peso 15%

| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| PCR-us | <1.0 mg/L | 1.0-2.0 | 2.0-3.0 | >3.0 |
| Ferritina (H) | 30-200 ng/mL | 200-300 | 300-500 ou <30 | >500 ou <15 |
| Ferritina (M) | 20-150 ng/mL | 150-200 | 200-300 ou <20 | >300 ou <10 |
| Ácido úrico (H) | <5.5 mg/dL | 5.5-6.5 | 6.5-7.5 | >7.5 |
| Ácido úrico (M) | <4.5 mg/dL | 4.5-5.5 | 5.5-6.5 | >6.5 |

## Domínio 4 — Perfil Lipídico (LIP) — Peso 15%

| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| HDL (H) | >50 mg/dL | 40-50 | 35-40 | <35 |
| HDL (M) | >60 mg/dL | 50-60 | 40-50 | <40 |
| Triglicerídeos | <100 mg/dL | 100-150 | 150-200 | >200 |
| Relação TG/HDL | <2.0 | 2.0-3.0 | 3.0-4.0 | >4.0 |

## Domínio 5 — Eixo Hormonal (HOR) — Peso 15%

### Homens
| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| Testosterona total | 500-900 ng/dL | 400-500 | 300-400 | <300 |
| SHBG | 20-40 nmol/L | 40-55 | 55-70 ou <20 | >70 ou <15 |
| Estradiol | 20-35 pg/mL | 35-45 | 45-60 ou <20 | >60 |
| Cortisol manhã | 10-18 µg/dL | 18-22 ou 6-10 | 22-25 ou <6 | >25 |
| TSH | 0.5-2.5 mUI/L | 2.5-4.0 | 4.0-6.0 | >6.0 ou <0.3 |

### Mulheres (fase folicular)
| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| Estradiol | 30-120 pg/mL | contextual | contextual | <20 |
| Progesterona (lútea) | >10 ng/mL | 5-10 | 2-5 | <2 |
| Testosterona | 15-50 ng/dL | contextual | contextual | contextual |
| Cortisol manhã | 10-18 µg/dL | 18-22 ou 6-10 | 22-25 ou <6 | >25 |
| TSH | 0.5-2.5 mUI/L | 2.5-4.0 | 4.0-6.0 | >6.0 ou <0.3 |

## Domínio 6 — Micronutrientes (MIC) — Peso 10%

| Marcador | Ótimo (90-100) | Bom (70-89) | Moderado (50-69) | Ruim (<50) |
|----------|---------------|-------------|-------------------|-----------|
| Vitamina D | 40-60 ng/mL | 30-40 | 20-30 | <20 |
| B12 | 500-1000 pg/mL | 300-500 | 200-300 | <200 |
| Magnésio | 2.0-2.5 mg/dL | 1.8-2.0 | 1.5-1.8 | <1.5 |
| Zinco | 80-120 µg/dL | 70-80 | 60-70 | <60 |

## Regras de Cálculo
1. Se marcador não disponível → usar média dos demais marcadores do domínio
2. Mínimo 2 marcadores por domínio para score válido
3. Se domínio inteiro sem dados → excluir e redistribuir peso proporcionalmente
4. Score geral = média ponderada arredondada para inteiro
5. Histórico deve manter todos os scores calculados (nunca deletar)

## Alertas Automáticos
- SMI caiu >10 pontos em 1 mês → ALERTA URGENTE ao médico
- Domínio individual <40 → ALERTA de domínio crítico
- 3 meses sem melhora → ALERTA de estagnação
- Marcador fora de range crítico → ALERTA laboratorial
