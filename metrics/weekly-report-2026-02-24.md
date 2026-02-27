# Weekly Metrics Report — Semana de 18–24 Fev 2026

**Gerado em:** 2026-02-24
**Owner:** PM + Data Scientist (Priya Sharma)

---

## Resumo Executivo
Semana mista. Demo com clientes Enterprise foi bem recebida e gerou 2 upgrades de Growth → Enterprise. Porém DAU caiu levemente após o feriado de terça, e o NLQ teve um incidente de dado incorreto que afetou 3 contas.

---

## North Star: Insights Acionados por Semana
| Semana | Insights acionados | WoW | vs. Meta Q1 |
|---|---|---|---|
| 10 fev – 16 fev | 3.420 | +4.0% | -43% |
| 17 fev – 23 fev | 3.380 | -1.2% | -44% |

**Análise:** Leve queda atribuída ao feriado de terça (17/02). Ajustando para dias úteis, crescimento ainda positivo (+1.8%).

---

## Engajamento

| Métrica | Atual | Semana anterior | Meta Q1 |
|---|---|---|---|
| DAU | 8.520 | 8.690 | 11.480 |
| MAU | 31.600 | 31.400 | — |
| DAU/MAU ratio | 26.9% | 27.7% | 35% |
| Sessões/usuário/semana | 4.0 | 4.2 | 5.0 |
| Tempo médio de sessão | 6m 50s | 6m 40s | 8m |

---

## AI Insights

| Métrica | Atual | Semana anterior | Meta Q1 |
|---|---|---|---|
| % usuários que abrem Insights 3x+/semana | 26% | 24% | 40% |
| % insights marcados como "úteis" | 25% | 23% | 40% |
| % insights marcados como "irrelevantes" | 46% | 49% | 20% |
| Latência média | 2.0s | 2.1s | 2.0s |

**Destaque:** Latência bateu a meta de 2.0s pela primeira vez. 🎉

---

## Incidente da Semana — NLQ Dado Incorreto
**Data:** 2026-02-19
**Impacto:** 3 contas (2 Growth, 1 Enterprise) receberam dados de MAU incorretos via NLQ
**Causa raiz:** Query gerada pelo modelo usou tabela errada após migração de schema da semana passada
**Resolução:** Bruno corrigiu o mapping em 4 horas. Contas notificadas por Ana Lima.
**Status:** Resolvido, mas confiança no NLQ afetada. Post-mortem agendado para sprint 43.

---

## Crescimento

| Métrica | Esta semana | Mês anterior |
|---|---|---|
| Novos clientes | 6 | 18 (mês) |
| Upgrades (Growth → Enterprise) | 2 | 1 (mês anterior) |
| Downgrades | 0 | 2 |
| Churns | 1 (Growth) | 6 |

**Destaque:** 2 upgrades em uma semana — acima da média mensal. Ambos vieram da demo de quinta.

---

## Alertas da Semana
🔴 **Incidente NLQ** — post-mortem necessário, confiança da feature em risco
🟡 **DAU caiu WoW** — avaliar se é feriado ou tendência (monitorar semana que vem)
🟢 **2 upgrades Enterprise** — demo de quinta gerou resultado direto
🟢 **Latência bateu meta de 2.0s**
