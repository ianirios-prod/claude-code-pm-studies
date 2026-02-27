# Command: /user-research

Analise as entrevistas de usuário fornecidas e gere um relatório de síntese no seguinte formato:

## Perfil dos Entrevistados
| Nome | Cargo | Empresa | Tempo de Cliente | Plano |
|---|---|---|---|---|

## Top 5 Dores (por frequência de menção)
1. **[Dor]** — Mencionada por X de Y usuários
   - Contexto: [detalhes]
   - Impacto no negócio: [churn risk / upgrade opportunity / NPS]

## Oportunidades de Produto
| Oportunidade | Usuários que pediram | Impacto Estimado | Esforço |
|---|---|---|---|

## Citações Mais Relevantes
> "[citação direta]" — [Nome, Cargo]

## Insights por Segmento
- **PMs técnicos:** [padrões]
- **PMs não-técnicos:** [padrões]
- **Team leads / VPs:** [padrões]

## Recomendações para o Roadmap
1. **Prioridade Alta:** [Feature / melhoria] — [justificativa baseada em dados das entrevistas]
2. **Prioridade Média:** [Feature / melhoria]
3. **Tech Debt com impacto em usuário:** [item]

## Sinais de Churn Risk
- [Usuário]: [motivo + probabilidade de churn]

---
**Regras:**
- Baseie todas as afirmações em evidências das entrevistas
- Quantifique quando possível ("3 de 3 usuários mencionaram X")
- Separe fatos de inferências
- Use o contexto do negócio em `context/business-info.md`
