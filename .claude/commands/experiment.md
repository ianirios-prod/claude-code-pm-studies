# Command: /experiment

Estruture um experimento (A/B test ou teste controlado) a partir da ideia ou problema descrito.

## Formato de Output

# Experimento #XXX — [Nome]

## Contexto
[Qual problema ou oportunidade motivou este experimento]

## Hipótese
Se [ação/mudança], então [resultado esperado], porque [raciocínio causal].

## Setup
| Grupo | Tamanho estimado | Tratamento |
|---|---|---|

**Segmentação:** [Quem entra no experimento e por quê]
**Duração:** [Mínimo para significância estatística — calcular com base no tráfego]

**Métrica primária:** [O que vai provar ou refutar a hipótese]
**Métricas secundárias:** [O que monitorar para efeitos colaterais]
**Guardrails:** [Métricas que, se piorarem, param o experimento]

## Critério de Sucesso
[Qual resultado mínimo justifica lançar para 100%]

## Riscos
- [Risco de execução ou interpretação]

## O que NÃO é esse experimento
[Esclarecer escopo para evitar confusão]

---
**Regras:**
- Hipótese deve ter causa e efeito explícitos — evitar "se melhorarmos X, será melhor"
- Sempre definir guardrails — experimentos podem melhorar uma métrica e piorar outra
- Calcular duração mínima baseado no tráfego real (referência: `metrics/`)
- Uma métrica primária apenas — múltiplas primárias levam a interpretações ambíguas
