# Tickets de Suporte — Fevereiro 2026
**Período:** 1–24 Fev 2026
**Total de tickets:** 47
**Tempo médio de resolução:** 6h (meta: 4h Enterprise, 24h Growth/Starter)

---

## Categorias

| Categoria | Tickets | % | Vs. Jan |
|---|---|---|---|
| NLQ — resposta incorreta ou incompleta | 18 | 38% | +60% |
| Performance / Latência | 8 | 17% | -50% |
| Setup e configuração de eventos | 7 | 15% | 0% |
| AI Insights — insight irrelevante | 6 | 13% | -25% |
| Billing e planos | 4 | 8% | +33% |
| Bug (outros) | 4 | 8% | 0% |

---

## Tickets Críticos do Mês

### Ticket #4821 — Dado incorreto NLQ (CRÍTICO)
**Cliente:** TechCorp Enterprise (ARR: $24.000)
**Data:** 2026-02-19
**Descrição:** NLQ retornou MAU de 45.000 quando o real era 12.000. Cliente usou dado em apresentação para board.
**Impacto:** Constrangimento com board. Cliente pediu reunião de crise.
**Resolução:** Bug identificado (mapping de tabela errado após migração). Corrigido em 4h. Desconto de 15% no próximo mês oferecido.
**Status:** Resolvido. Cliente satisfeito com resposta rápida.

### Ticket #4798 — Perda de dados de tracking (ALTO)
**Cliente:** ShopBR Growth (ARR: $7.200)
**Data:** 2026-02-14
**Descrição:** Eventos de checkout não estavam sendo registrados por 48h. Cliente percebeu quando funil mostrou conversão 0%.
**Impacto:** 2 dias de dados perdidos, impossível de recuperar.
**Resolução:** Bug no SDK mobile v2.1.3. Hotfix lançado. SDK v2.1.4 publicado.
**Status:** Resolvido. Cliente pediu compensação — 1 mês grátis oferecido.

### Ticket #4812 — NLQ não responde perguntas causais (MÉDIO)
**Cliente:** FinanceApp Growth (ARR: $7.200)
**Data:** 2026-02-21
**Descrição:** "Por que meu churn aumentou em janeiro?" — NLQ retornou "Não tenho dados suficientes para responder" mas os dados existem.
**Impacto:** PM perdeu confiança na feature. Considerando downgrade.
**Resolução:** Explicamos limitação atual do NLQ (não suporta análise causal). Cliente insatisfeito.
**Status:** Em acompanhamento. NLQ v2 está no roadmap Q2 — comunicado ao cliente.

---

## Tendências Preocupantes
1. **NLQ tickets +60% MoM** — principal driver de insatisfação. Incidente de dado incorreto acelerou.
2. **Billing tickets +33%** — investigar se há confusão sobre limites de plano ou cobranças inesperadas.

## Tendências Positivas
1. **Performance tickets -50%** — reflexo direto da otimização de latência do Sprint 42.
2. **AI Insights tickets -25%** — card de contexto ajudou a reduzir percepção de insights irrelevantes.
