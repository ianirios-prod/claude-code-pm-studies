# Análise Competitiva — Mixpanel vs. Amplitude
**Data:** 2026-02-15
**Contexto:** Foco em funcionalidades de IA — como competidores estão respondendo à nossa proposta de valor

---

## Mixpanel

### AI / ML Features
- **Mixpanel AI (lançado Q3 2025):** Resumos automáticos de relatórios em linguagem natural
- **Spark:** Sugestão de eventos para trackar baseado no código do app
- **Signal:** Identifica quais comportamentos predizem conversão ou churn

### Pontos Fortes vs. DataFlow
- Ecossistema de integrações muito maior (200+ integrações vs. nossos ~15)
- Brand recognition — é o padrão de mercado para analytics
- Documentação excelente, comunidade grande
- Pricing mais flexível (pay-as-you-go por eventos)

### Pontos Fracos vs. DataFlow
- AI é add-on, não nativo — parece "colado"
- NLQ não existe — usuários ainda escrevem queries manualmente
- UX desatualizada — muitas opções, curva de aprendizado alta
- Insights são descritivos, não acionáveis ("DAU subiu 5%" sem contexto)

### Pricing (fev/2026)
- Free: até 20M eventos/mês, features básicas
- Growth: $28/mês por usuário (~$140/mês para 5 usuários) — mais caro que nós no mesmo volume
- Enterprise: Custom

---

## Amplitude

### AI / ML Features
- **Amplitude AI (lançado Q2 2025):** Geração automática de charts a partir de perguntas em linguagem natural
- **Predict:** Modelos de ML para prever churn e LTV
- **Pathfinder AI:** Sugere jornadas do usuário para otimizar

### Pontos Fortes vs. DataFlow
- Amplitude AI é mais maduro que nosso NLQ — melhor em perguntas analíticas
- Predict é genuinamente diferenciado — nenhum concorrente tem isso tão bom
- Forte no segmento Enterprise — mais recursos de governance e permissões
- Integração com data warehouses (Snowflake, BigQuery) — nós não temos

### Pontos Fracos vs. DataFlow
- Preço alto — Enterprise começa em ~$2.000/mês
- Complexidade — time precisa de treinamento longo
- Insights ainda requerem análise humana para ser acionáveis
- Sem notificações proativas (o Slack deles é básico)

### Pricing (fev/2026)
- Starter: Gratuito, limitado
- Plus: $61/mês (muito limitado)
- Growth: Custom (estimado ~$800–1.200/mês para nosso ICP)
- Enterprise: Custom ($2.000+)

---

## Matriz de Posicionamento

| Capacidade | DataFlow AI | Mixpanel | Amplitude |
|---|---|---|---|
| NLQ para perguntas simples | 🟡 Médio | ❌ Não tem | 🟢 Bom |
| NLQ para perguntas causais | ❌ Não tem | ❌ Não tem | 🟡 Médio |
| Insights proativos (push) | 🟢 Bom | ❌ Não tem | ❌ Não tem |
| Personalização de insights | 🔨 Em construção | ❌ Não tem | ❌ Não tem |
| Previsão de churn/LTV | ❌ Não tem | 🟡 Médio | 🟢 Bom |
| Integrações | 🔴 Fraco | 🟢 Ótimo | 🟢 Bom |
| UX / Facilidade de uso | 🟢 Bom | 🟡 Médio | 🟡 Médio |
| Preço para nosso ICP | 🟢 Competitivo | 🟡 Similar | 🔴 Caro |
| Onboarding / Documentação | 🔴 Fraco | 🟢 Ótimo | 🟢 Bom |

---

## Implicações para Roadmap
1. **Defensivo:** NLQ para perguntas causais — Amplitude está à frente, risco de perder deals
2. **Ofensivo:** Personalização por OKR + notificações proativas — whitespace que nenhum competidor tem
3. **Urgente:** Documentação e onboarding — estamos claramente atrás dos dois
4. **Longo prazo:** Integração com data warehouses — blocker para Enterprise acima de $50K ARR
