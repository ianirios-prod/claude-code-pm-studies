# Experimento #001 — Email Digest Semanal de Insights
**Status:** Concluído ✅
**Período:** 6–27 Jan 2026 (3 semanas)
**Owner:** PM + Priya Sharma (Data Scientist)

---

## Hipótese
Se enviarmos um email digest semanal com os top 5 insights da semana para usuários inativos (não acessaram o app em 7+ dias), então aumentaremos o re-engajamento em pelo menos 15%, porque esses usuários estão perdendo valor por não acessar ativamente.

---

## Setup do Experimento

| Grupo | Tamanho | Tratamento |
|---|---|---|
| Controle | 420 usuários | Sem email |
| Variante A | 418 usuários | Email digest toda segunda-feira 9h |
| Variante B | 421 usuários | Email digest toda quarta-feira 9h |

**Critério de segmentação:** Usuários ativos no mês mas sem login nos últimos 7 dias
**Métrica primária:** Re-engajamento em 7 dias (login após receber email)
**Métricas secundárias:** Abertura de email, clique em insight, sessões na semana seguinte

---

## Resultados

| Métrica | Controle | Variante A (seg) | Variante B (qua) |
|---|---|---|---|
| Re-engajamento 7 dias | 8.2% | 19.4% | 22.1% |
| Taxa de abertura | — | 34% | 31% |
| Click-through rate | — | 12% | 14% |
| Sessões semana seguinte | 1.1 | 2.3 | 2.6 |
| Unsubscribe rate | — | 3.2% | 2.8% |

**Significância estatística:** p < 0.01 para ambas variantes vs. controle ✅

---

## Conclusões

✅ **Hipótese confirmada** — ambas variantes superaram a meta de 15% de re-engajamento.

**Variante B (quarta-feira) foi melhor** — 22.1% de re-engajamento vs. 19.4% da variante A. Hipótese: segunda-feira é muito cedo na semana, usuários ainda estão se organizando.

**Qualidade do re-engajamento é alta** — sessões da semana seguinte mais que dobraram (2.6 vs. 1.1 no controle). Não é engajamento vazio.

**Risco identificado:** 3.2% de unsubscribe na variante A é alto. Variante B teve 2.8% — aceitável mas deve ser monitorado.

---

## Decisão
**Lançar para 100% da base** usando o formato da Variante B (quarta-feira, 9h).

**Próximos passos:**
- Personalizar os 5 insights selecionados por relevância para o usuário (hoje é randômico)
- Testar frequência: semanal vs. quinzenal para reduzir unsubscribes
- Criar versão para usuários ativos (insights que eles não viram, não apenas re-engajamento)
