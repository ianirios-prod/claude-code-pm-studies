# Stack de IA para Technical AI PM — Guia Completo

Este guia combina o que o vídeo recomendou com expansões para um PM técnico que trabalha com produtos de IA.

---

## A Lógica do Stack

Não existe uma ferramenta que faz tudo bem. A chave é entender *o que cada tool faz melhor* e usar a certa para cada tipo de trabalho.

```
Tipo de trabalho          →  Ferramenta certa
─────────────────────────────────────────────
Análise, escrita, PRDs    →  Claude Code (Pro)
Coding pesado             →  Cursor
Automações recorrentes    →  N8N
Protótipos rápidos de UI  →  v0 ou Cursor
```

---

## Claude Code — Para que Usar

### ✅ Use para:
- Análise de user research (comparar entrevistas, encontrar padrões)
- Escrever e iterar PRDs com contexto do negócio
- Sintetizar reuniões e gerar action items
- Pesquisa competitiva com web search
- Análise de métricas e diagnóstico de alertas
- Rascunhos de comunicação (Slack, emails, release notes)
- Criar protótipos para validar ideias com stakeholders
- Estruturar experimentos e evals de LLM
- Qualquer tarefa pontual onde você quer estar no loop

### ❌ Não use para:
- Automações que precisam rodar sem você (use N8N)
- Coding de produção sem engineer review
- Decisões estratégicas (Claude prepara, você decide)
- Dados sensíveis de clientes reais sem revisar privacidade

---

## N8N — Para que Usar

### ✅ Use para:
- Monitorar competidores semanalmente (busca automática + sumarização)
- Digest de posts do Reddit/Twitter sobre seu mercado
- Alertas automáticos quando métricas saem do range
- Processar tickets de suporte e categorizar automaticamente
- Enviar resumo semanal de métricas para Slack do time
- Qualquer coisa que você faz todo dia/semana da mesma forma

### ❌ Não use para:
- Tarefas únicas e pontuais (desperdício de setup)
- Trabalho criativo ou estratégico
- Coisas onde o contexto muda muito a cada vez

---

## Cursor — Para que Usar

### ✅ Use para:
- Desenvolvimento de features reais no codebase do produto
- Debug de código complexo
- Refatoração com compreensão do contexto do repo
- Pair programming assíncrono com engenheiros
- Quando precisar de modelos Opus para coding mais complexo

### Como PM técnico (não full-time dev):
Use Cursor para explorar o codebase do seu produto — entender como funciona, fazer perguntas sobre arquitetura, propor mudanças pequenas para discutir com engenharia. Não para fazer deploy sem review de engenheiro.

---

## v0 / Lovable — Para que Usar

### ✅ Use para:
- Protótipos de UI em 30 segundos para validar com stakeholders
- Quando você precisa de algo visual rápido sem precisar de qualidade de código
- Wireframes interativos que vão além do Figma estático

### Diferença vs. Claude Code para protótipos:
- v0: mais rápido (30s vs. 5 min), mais visual, menos flexível
- Claude Code: mais lento, mas pode criar lógica real, integrar com APIs, ter estado

---

## Para Technical AI PM: O Stack Específico

Como PM de produto de IA, você tem necessidades extras além do PM tradicional:

### 1. Avaliação de Modelos
Use Claude Code para:
```
"Crie 3 variações de prompt para [feature X].
Rode cada uma contra estes 10 exemplos de input usando GPT-4o, Claude Sonnet e Gemini.
Salve os resultados em experiments/eval-[nome].md para comparação."
```

### 2. Análise de Qualidade de LLM em Produção
```
"Analise estes 50 logs de resposta do nosso modelo de insights.
Categorize: correto, parcialmente correto, incorreto.
Para os incorretos, identifique o padrão de falha mais comum."
```

### 3. Estruturar Evals antes de Lançar Features de IA
```
"Com base no PRD desta feature e nas entrevistas de usuário,
crie um conjunto de 20 casos de teste para avaliar a qualidade
dos insights gerados. Inclua casos edge e casos de falha esperada."
```

### 4. Diagnóstico de Incidentes de IA
```
"Aqui estão os logs do incidente de NLQ de 19/02.
Analise e identifique: causa raiz, extensão do impacto,
pattern de inputs que triggeram o erro, e recomendações de fix."
```

---

## Quando o Stack Evolui

O vídeo foi honesto: *"Multi-agent things will be more powerful as models improve."*

Hoje (2026): Humano no loop, agents táticos, supervise sempre.
Em 12-18 meses: Chains mais longas serão confiáveis, supervision diminui.
Em 3 anos: Agents autônomos para tarefas bem definidas serão o padrão.

**Como se preparar agora:**
Construir o hábito de context engineering bem feito (CLAUDE.md rico, pastas organizadas, commands bem definidos) é o que vai te deixar pronto para aproveitar os agents mais autônomos quando chegarem. Quem já tem o contexto organizado vai escalar muito mais rápido.
