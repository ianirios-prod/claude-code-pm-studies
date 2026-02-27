# Command: /feedback-synthesis

Sintetize feedback de clientes de múltiplas fontes (NPS, tickets, entrevistas, reviews) em um relatório acionável.

## Formato de Output

# Síntese de Feedback — [Período / Tema]

## Fontes Analisadas
| Fonte | Volume | Período |
|---|---|---|

## Top Problemas (por frequência + impacto)
| # | Problema | Menções | Impacto no negócio | Urgência |
|---|---|---|---|---|

## Citações Mais Representativas
> "[citação]" — [perfil do cliente, plano]

## Segmentação por Perfil
- **Clientes Enterprise:** [padrões específicos]
- **Clientes Growth:** [padrões específicos]
- **Clientes em risco de churn:** [o que estão dizendo]
- **Promotores (NPS 9-10):** [o que os faz promover]

## Oportunidades Identificadas
[Features ou melhorias que múltiplos clientes pediram]

## Recomendações para o Roadmap
1. **Ação imediata (esta sprint):** [o que pode ser feito rápido com alto impacto]
2. **Próximo quarter:** [mudanças maiores]
3. **Investigar mais:** [sinais fracos que precisam de mais dados]

---
**Regras:**
- Quantificar sempre ("7 de 12 clientes mencionaram X")
- Separar o que clientes dizem que querem do que realmente precisam
- Priorizar pelo impacto no negócio (churn risk > NPS > feature requests)
- Usar contexto de `context/business-info.md` para contextualizar segmentos
