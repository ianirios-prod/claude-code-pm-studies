# Executive Review — Q1 2026 Progress
**Data:** 2026-02-26
**Participantes:** PM (você), Rafael Mendes (CTO), Fernanda Costa (CEO), Lucas Alves (CFO)
**Objetivo:** Update de meio de quarter para o board — progresso nos OKRs, riscos, decisões necessárias

---

## Update de OKRs (6 semanas de 13)

### OKR 1: Aumentar engajamento com AI Insights
| Key Result | Meta | Atual | Projeção final |
|---|---|---|---|
| DAU abrindo AI Insights | 45% | 26% | ~35% ⚠️ |
| % insights marcados úteis | 40% | 25% | ~32% ⚠️ |
| % feedback negativo | 20% | 46% | ~30% ⚠️ |

**Narrativa:** Estamos progredindo mas abaixo do pace necessário. O lançamento do card de contexto gerou melhora visível (feedback negativo caiu de 60% → 46%). A personalização por OKR (Sprint 44, início em 10/03) deve ser o maior driver — projetamos +15pp em % úteis.

### OKR 2: Reduzir churn
| Key Result | Meta | Atual | Projeção final |
|---|---|---|---|
| Churn mensal | 1.8% | 2.1% | ~1.9% 🟡 |
| NPS | 55 | 45 | ~50 🟡 |
| Contas Enterprise em risco | 3 | 6 | ~4 🟡 |

**Narrativa:** Churn melhorou de 2.3% → 2.1% mas ainda acima da meta. 2 upgrades Enterprise esta semana são positivos. Risco: incidente do NLQ afetou 3 contas — Ana Lima em acompanhamento ativo.

### OKR 3: Base técnica escalável
| Key Result | Meta | Atual | Projeção final |
|---|---|---|---|
| Latência AI Insights | 2.0s | 2.0s | ✅ Atingido |
| Custo por insight | $0.010 | $0.018 | ~$0.013 🟡 |
| Eval pipeline | 100% | 0% | 100% 🟢 (Sprint 43) |

---

## Riscos Principais

### 🔴 Risco Alto — NLQ Confiabilidade
Incidente de dado incorreto em 19/02 afetou conta Enterprise de $24K ARR. NLQ tickets subiram 60% MoM. Sem NLQ v2 no roadmap até Q2, risco de churn de contas que compraram por causa do NLQ.
**Decisão necessária:** Antecipar NLQ v2 para Q1 ou comunicar clientes proativamente sobre limitações?

### 🟡 Risco Médio — Escala sem Eval Pipeline
Lançamos AI Insights para base Enterprise sem eval automatizado. Hoje a Priya S. faz revisão manual de 50 insights/semana. Com crescimento, isso não escala.
**Status:** Sprint 43 entrega eval pipeline — risco resolvido em 2 semanas.

### 🟡 Risco Médio — OKRs abaixo do pace
Projeção atual indica que não vamos atingir as metas de engajamento em Q1. Personalização por OKR é o principal driver faltante.
**Status:** Dependente de Sprint 44 (início 10/03) entregar conforme planejado.

---

## Pedidos de Decisão ao Board

1. **NLQ v2 — antecipar para Q1 ou Q2?**
   - Antecipar para Q1: Atrasa personalização por OKR em 2 sprints, risco de não entregar nenhum dos dois
   - Manter em Q2: Risco de churn de contas NLQ-dependentes (~8 contas identificadas, ~$48K ARR)
   - **Recomendação do PM:** Manter em Q2, mas comunicar proativamente clientes com plano de mitigação

2. **Contratar Eng adicional para Q2?**
   - Q2 tem roadmap muito carregado (NLQ v2, Jira, webhooks, mobile)
   - Estamos com 3 engenheiros — gargalo está se tornando claro
   - **Recomendação:** Abrir 1 posição sênior agora para onboarding em abril

---

## Próximo Executive Review
**Data:** 2026-03-26 (final de Q1)
**Foco:** Resultado final dos OKRs + planejamento de Q2
