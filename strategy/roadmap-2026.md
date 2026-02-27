# Roadmap de Produto — 2026
**Última atualização:** 2026-02-20
**Owner:** PM
**Horizonte:** Q1–Q3 2026 (Q4 é planejamento em setembro)

---

## Status dos Temas Estratégicos

| Tema | Q1 | Q2 | Q3 |
|---|---|---|---|
| AI Insights — Personalização | 🔨 Construindo | 🔮 Planejado | — |
| NLQ — Qualidade e Confiabilidade | 🔮 Planejado | 🔨 Construindo | — |
| Integrações (Slack, Jira, Webhooks) | 🔨 Parcial | 🔨 Construindo | — |
| Mobile Experience | — | 🔮 Planejado | 🔨 Construindo |
| Plataforma (Evals, Custos, Performance) | 🔨 Construindo | — | — |

---

## Q1 2026 — Detalhado (Jan–Mar)

### ✅ Entregue
- Parallelização de LLM calls (latência 4.2s → 2.1s)
- Card "por que esse insight apareceu" (v1 simplificada)
- Notificação proativa no Slack

### 🔨 Em construção
- **Eval pipeline automatizado** (Sprint 43) — base para escalar IA com qualidade
- **Prompt optimization** (Sprint 43) — reduzir custo e latência
- **Personalização de insights por OKR** (Sprint 44) — maior pedido dos Enterprise

### 🔮 Planejado para Q1
- **Onboarding guiado** — reduzir tempo de setup de 3 dias para < 1 hora
- **NLQ v2** — suporte a perguntas causais ("por que X aconteceu?")

---

## Q2 2026 — Planejado (Abr–Jun)

### Tema Principal: NLQ de Qualidade
- NLQ com raciocínio multi-step para perguntas causais
- Indicador de confiança nas respostas ("alta confiança" / "incerto")
- Histórico de queries salvas

### Integrações
- Integração Jira bidirecional (criar ticket a partir de insight)
- Webhook API para dashboards externos (pedido da Priya Chen)
- Google Sheets export

### Monetização
- AI Insights completo no plano Growth (hoje só no Enterprise)
- Nova tier: "Professional" entre Growth e Enterprise

---

## Q3 2026 — Direção (Jul–Set)
- Mobile app v1 (iOS first)
- Colaboração em insights (compartilhar, comentar, atribuir)
- AI Forecasting (projeções baseadas em tendências históricas)

---

## O que Não Está no Roadmap (e Por Quê)
| Feature | Motivo de não estar |
|---|---|
| Data warehouse connector (Snowflake, BigQuery direto) | Alto esforço, baixa demanda no ICP atual |
| White-label | Distrai do produto core, pedido de 1 cliente apenas |
| SSO Enterprise | Planejado para Q2 se deals Enterprise aumentarem |
