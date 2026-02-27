# Experimento #002 — Onboarding Checklist In-App
**Status:** Em andamento 🔨
**Período:** 17 Fev – 10 Mar 2026
**Owner:** PM + Camila Torres (Designer)

---

## Contexto
NPS survey de Q4 e entrevistas com João Silva mostraram que novos usuários levam até 3 dias para configurar o primeiro funil. Isso aumenta time-to-value e risco de churn precoce (primeiros 30 dias).

---

## Hipótese
Se mostrarmos um checklist de onboarding in-app para novos usuários (primeiros 7 dias), então reduziremos o tempo até primeira análise de funil de 3 dias para menos de 4 horas, porque o checklist vai guiar os usuários pelos passos essenciais sem precisar ler a documentação.

---

## Setup do Experimento

| Grupo | Tamanho | Tratamento |
|---|---|---|
| Controle | Novos usuários sem checklist | Experiência atual |
| Variante A | Novos usuários com checklist | Checklist de 5 passos no sidebar |

**Segmentação:** Todos os novos usuários que ativaram conta a partir de 17/02
**Duração estimada:** 3 semanas (até ter 100+ usuários por grupo)

**Checklist — 5 passos:**
1. Instale o SDK (com link para documentação simplificada)
2. Configure seu primeiro evento (template sugerido)
3. Crie seu primeiro funil
4. Explore o AI Insights Feed
5. Conecte o Slack para notificações

**Métricas primárias:**
- Tempo até primeira análise de funil completada
- % de usuários que completam o funil nos primeiros 7 dias

**Métricas secundárias:**
- Tickets de suporte de novos usuários (esperamos redução)
- Retenção D7 e D30
- NPS dos primeiros 30 dias

---

## Status Atual (2026-02-24)
- Variante A lançada para novos usuários desde 17/02
- **Tamanho atual:** Controle: 28 usuários | Variante A: 31 usuários
- **Resultado parcial (ainda não significativo):**
  - Tempo médio até 1º funil: Controle 58h | Variante A 18h
  - % completam funil em 7 dias: Controle 31% | Variante A 61%

**⚠️ Resultado parcial muito positivo, mas n pequeno. Não concluir ainda.**

---

## Riscos
- **Checklist pode ser ignorado:** Se usuários fecharem e não voltarem, não teremos efeito
- **Qualidade do funil pode ser baixa:** Usuários podem completar o checklist "por completar" sem entender o produto
- **Generalização:** Usuários que ativam em fevereiro podem ter perfil diferente dos demais

---

## Próximas Ações
- Continuar coleta até 10/03
- Entrevistar 3 usuários da Variante A para entender como usaram o checklist
- Preparar análise final para sprint review de 10/03
