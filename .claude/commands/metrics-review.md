# Command: /metrics-review

Analise os relatórios de métricas fornecidos e gere um diagnóstico estruturado.

## Formato de Output

# Diagnóstico de Métricas — [Período]

## North Star
[Status da north star metric com contexto e tendência]

## O que está indo bem 🟢
- [Métrica]: [valor] — [por que importa e o que causou]

## O que precisa de atenção 🟡
- [Métrica]: [valor] — [contexto e próximo passo]

## Alertas críticos 🔴
- [Métrica]: [valor] — [impacto e ação imediata necessária]

## Correlações Identificadas
- [Evento X] parece estar correlacionado com [mudança em métrica Y]

## Recomendações
1. [Ação imediata — quem, o quê, quando]
2. [Investigação necessária]
3. [Monitorar de perto]

---
**Regras:**
- Sempre comparar com baseline e meta, não só com semana anterior
- Separar causalidade de correlação claramente
- Cada alerta deve ter um próximo passo claro
- Contextualizar com eventos da semana (deploys, campanhas, feriados)
