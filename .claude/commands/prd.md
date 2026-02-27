# Command: /prd

Gere um PRD completo para a feature descrita, seguindo este template. Use o contexto em `context/business-info.md` e o estilo em `context/writing-styles.md`. Siga o exemplo em `prds/prd-example-ai-insights.md`.

---

# PRD: [Nome da Feature]

**Status:** Draft
**Author:** PM
**Last Updated:** [data]
**Target Release:** [sprint / data]

## Problem Statement
[1 parágrafo: qual dor estamos resolvendo, para quem, e qual a evidência que temos disso]

## Goals
| Goal | Metric | Baseline | Target |
|------|--------|----------|--------|

## Non-Goals
- [O que explicitamente NÃO está no escopo]

## User Stories
- **As a [persona]**, I want to [ação] so that [benefício]

## Proposed Solution
[Descrição da solução com fases se necessário]

## Technical Approach
[Decisões técnicas relevantes para o PM: modelo de dados, APIs, infra]

## Acceptance Criteria
- [ ] [Critério mensurável e testável]

## Risks
| Risk | Likelihood | Impact | Mitigation |

## Dependencies
- [O que precisa estar pronto antes]

## Open Questions
- [Perguntas que precisam ser respondidas antes do dev começar]

---
**Regras:**
- Sempre incluir baseline e target nas métricas
- Acceptance criteria devem ser testáveis (evite "deve ser rápido" → use "latência < 2s")
- Se houver user research relacionado em `user-research/`, referencie as entrevistas
- Non-goals são tão importantes quanto goals — seja explícito
