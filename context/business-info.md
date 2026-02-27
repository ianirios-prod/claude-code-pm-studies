# DataFlow AI — Business Context

## Produto
DataFlow AI é uma plataforma de analytics inteligente que usa IA para transformar eventos de comportamento de usuário em insights acionáveis para times de produto.

### Features Principais
1. **Event Tracking SDK** — captura automática de eventos no app (web/mobile)
2. **AI Insights Feed** — feed personalizado com anomalias, tendências e oportunidades detectadas por IA (em desenvolvimento)
3. **Funnel Analyzer** — análise de funis com sugestões automáticas de otimização
4. **Cohort Intelligence** — segmentação automática de usuários por comportamento
5. **Natural Language Query** — perguntas em linguagem natural sobre os dados ("Por que o churn aumentou essa semana?")

## Mercado e Competidores
- **Concorrentes diretos:** Mixpanel, Amplitude, PostHog
- **Diferenciação:** IA nativa (não é um add-on), melhor UX para PMs não-técnicos
- **ICP (Ideal Customer Profile):** Tech companies B2B, 50–500 funcionários, time de produto de 3–15 pessoas

## Métricas de Produto (baseline Q4 2025)
- DAU: 8,200 usuários ativos/dia
- MAU: 31,000
- NPS: 42
- Churn mensal: 2.3%
- ARPU: $890/mês
- Feature mais usada: Funnel Analyzer (68% dos usuários ativos)
- Feature menos usada: Natural Language Query (12% dos usuários ativos)

## Planos
- **Starter:** $199/mês — até 1M eventos/mês, 5 usuários
- **Growth:** $599/mês — até 10M eventos/mês, 20 usuários, AI Insights básico
- **Enterprise:** Custom — eventos ilimitados, usuários ilimitados, AI Insights completo, SLA

## Tech Stack
- Backend: Python (FastAPI), PostgreSQL, BigQuery, Redis
- Frontend: React, TypeScript, D3.js
- AI/ML: Claude claude-sonnet-4-6 (insights), GPT-4o (NLQ), modelos próprios de anomaly detection
- Infra: GCP, Kubernetes
- Integrations: Segment, Amplitude (import), Slack, Jira, Linear
