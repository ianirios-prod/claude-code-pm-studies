# Entrevista de Usuário — Ana Martins
**Data:** 2026-02-10
**Duração:** 45 minutos
**Entrevistador:** (PM)
**Perfil:** Head of Product, fintech de pagamentos, 200 funcionários, cliente há 8 meses (plano Growth)

---

## Contexto
Ana lidera um time de 4 PMs. Usa DataFlow AI principalmente para análise de funis de conversão e monitoramento de métricas pós-deploy.

---

## Transcrição Resumida

**PM:** Como você usa o DataFlow hoje no seu dia a dia?

**Ana:** Todo dia de manhã abro o dashboard pra ver se aconteceu alguma coisa estranha durante a noite. A gente tem um funil de cadastro que é crítico — qualquer queda de 5% eu preciso saber na hora. Mas hoje eu fico olhando pra uma tela esperando ver se tem algo errado. É reativo demais.

**PM:** O que seria o ideal pra você?

**Ana:** Quero que o sistema me avise *antes* de eu precisar olhar. Tipo, chega um Slack pra mim às 7h dizendo "atenção, etapa 3 do funil de cadastro caiu 12% comparado à média dos últimos 30 dias, provavelmente relacionado ao deploy de ontem às 23h". Não quero ter que ir atrás da informação.

**PM:** Você já usou o AI Insights? (feature em beta)

**Ana:** Tentei, mas os insights que ele me dá são muito genéricos. "Seu DAU aumentou 3%." Ok, mas por quê? De onde veio? Qual segmento? Me dê o contexto. Sem contexto não consigo fazer nada com essa informação.

**PM:** O que você acha mais valioso hoje na plataforma?

**Ana:** O Funnel Analyzer com certeza. É o que eu uso todo dia. Consigo entender o funil em 2 minutos em vez de escrever SQL por meia hora. Isso salva minha vida.

**PM:** O que te faria recomendar o DataFlow para outros PMs?

**Ana:** Se o AI Insights melhorasse pra dar contexto real e viesse com notificações proativas no Slack, eu recomendaria pra todo mundo. Hoje eu fico com vergonha de indicar porque sei que as pessoas vão perguntar "mas por que esse insight apareceu?" e eu não sei explicar.

**PM:** Quais são as maiores dores hoje?

**Ana:**
1. Insights sem contexto — número sem explicação não é insight
2. Latência — às vezes demora 5 segundos pra carregar um insight. Minha atenção já foi embora
3. Falta de integração com o Jira — quando descubro um problema, tenho que criar o ticket manualmente
4. Mobile não funciona bem — eu acesso pelo celular às vezes e a experiência é péssima

---

## Principais Insights
- **Dor #1:** Insights reativos vs. proativos — quer ser alertada, não ficar procurando
- **Dor #2:** Falta de contexto nos insights de IA ("por que esse insight apareceu?")
- **Comportamento:** Usa o produto toda manhã, mas de forma defensiva (procurar problemas)
- **Feature favorita:** Funnel Analyzer — ROI claro (economiza SQL)
- **Blocker de NPS:** Latência e falta de contexto nos insights de IA
- **Oportunidade:** Integração Slack proativa + contexto nos insights = potencial advocate
