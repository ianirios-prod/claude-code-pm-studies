# North Star Metric — DataFlow AI

## Nossa North Star
**"Número de insights acionados por semana"**

Definição: Um insight é "acionado" quando o usuário clica em "investigar", cria um ticket a partir dele, ou o marca como "útil".

### Por que essa métrica?
- Captura valor entregue, não só uso passivo
- Um usuário que abre o app mas ignora todos os insights não está recebendo valor
- Alinha produto, engenharia e CS em torno da mesma pergunta: "os insights estão sendo úteis?"

### Baseline e Meta
| Período | Insights acionados/semana | Nota |
|---|---|---|
| Q3 2025 | 1.200 | Pré-lançamento AI Insights |
| Q4 2025 | 2.800 | Lançamento AI Insights v1 |
| Hoje (fev/26) | 3.400 | |
| Meta Q1 2026 | 6.000 | Com personalização por OKR |
| Meta 2026 | 15.000 | Com NLQ v2 + mobile |

---

## Métricas de Suporte (Input Metrics)

### Engajamento
- DAU/MAU ratio (meta: > 35%)
- % usuários que abrem AI Insights ao menos 3x/semana (meta: 40%)
- Tempo médio de sessão (meta: > 8 minutos)

### Qualidade da IA
- % insights marcados como "úteis" (meta: > 40%)
- % insights marcados como "irrelevantes" (meta: < 20%)
- Latência média do AI Insights (meta: < 2s)

### Retenção
- Churn mensal (meta: < 1.8%)
- NPS (meta: > 55)
- Logo retention (meta: > 95%)

### Crescimento
- Novos clientes/mês (meta: 25)
- Expansão de receita (upgrades) — % da receita nova (meta: 30%)
- CAC payback period (meta: < 8 meses)

---

## Métricas que Deliberadamente Não Usamos como North Star
| Métrica | Por que não |
|---|---|
| MAU | Usuários mensais não capturam engajamento real — alguém pode logar 1x/mês |
| Número de eventos trackados | Métrica de infra, não de valor entregue |
| Receita | Lagging indicator — quando a receita cai, já é tarde demais para agir |
| Page views | Vanity metric — não reflete se o usuário recebeu valor |
