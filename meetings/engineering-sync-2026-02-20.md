# Engineering Sync — Performance & Tech Debt
**Data:** 2026-02-20
**Participantes:** PM (você), Bruno Carvalho (Eng Lead), Priya Sharma (Data Scientist)
**Duração:** 30 minutos

---

## Transcrição

**Bruno:** Boa notícia: cache otimizado, latência média em 2.1s. Mas preciso conversar sobre tech debt acumulado.

**PM:** Ótimo trabalho. Fala sobre o tech debt.

**Bruno:** Três problemas que vão nos bater no rosto se não endereçarmos:
1. O prompt de insights cresceu muito. Hoje tem 4.200 tokens de contexto pra cada insight. Isso é caro e lento.
2. Não temos evals automáticos. Priya S. valida os insights manualmente — não escala.
3. O modelo de anomaly detection não foi retreinado desde outubro. Os dados de comportamento mudaram muito com o lançamento da nova feature de funil.

**Priya S.:** Confirmo o item 2. Hoje eu reviso cerca de 50 insights por semana manualmente. Quando lançarmos pra todos os Enterprise, vão ser 500+. Não tem como.

**PM:** Que investimento você estima pra resolver cada um?

**Bruno:**
- Prompt optimization: 3 dias, pode reduzir custo em 40% e latência em 0.3s
- Eval pipeline: 5 dias, mas vai ser a base de tudo que vem depois
- Retreinamento do modelo: Priya S. é quem sabe estimar

**Priya S.:** Retreinamento com os dados novos: 4 dias de trabalho + 2 dias de GPU. Mas precisa de validação humana depois, mais 2 dias.

**PM:** Então temos ~20 dias de trabalho técnico crítico que não está no roadmap atual. Preciso priorizar isso vs. personalização por OKR que o Rafael pediu ontem.

**Bruno:** Minha recomendação: se a gente não fizer o eval pipeline, a personalização por OKR vai ser construída sobre areia. A gente vai lançar e não vai saber se está funcionando.

**PM:** Bom ponto. Vou levar pro Rafael essa trade-off. Proposta: sprint 43 faz eval pipeline + prompt optimization. Sprint 44 começa personalização por OKR em cima de uma base sólida.

**Bruno:** Apoio totalmente.

**Priya S.:** Mesma coisa. Prefiro construir certo do que rápido.

---

## Riscos Identificados
| Risco | Probabilidade | Impacto | Mitigação |
|---|---|---|---|
| Custo de LLM explode com escala | Alta | Alto | Prompt optimization na sprint 43 |
| Insights ruins chegam em produção sem detecção | Alta | Alto | Eval pipeline na sprint 43 |
| Modelo de anomaly detection desatualizado | Média | Alto | Retreinamento Q1 |
| Rafael insiste em OKR personalization pra sprint 43 | Média | Médio | Apresentar trade-off claramente |

## Action Items
| Responsável | Ação | Prazo |
|---|---|---|
| PM | Apresentar trade-off tech debt vs. OKR personalization ao Rafael | 2026-02-21 |
| Bruno | Estimar custo atual de LLM/mês e projeção com escala | 2026-02-21 |
| Priya S. | Rascunho de arquitetura do eval pipeline | 2026-02-22 |
