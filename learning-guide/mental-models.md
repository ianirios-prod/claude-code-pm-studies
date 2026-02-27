# Mental Models — Como Pensar sobre Claude Code

Estes são os conceitos centrais do vídeo + expansões para um Technical AI PM.

---

## 1. Prompt Engineering → Context Engineering

**O que o vídeo disse:**
> "We've moved from prompt engineering into context engineering. What you can give the LLM to work with is so key in what it's able to actually do."

**O que significa:**
Prompt engineering é sobre *como você pergunta*. Context engineering é sobre *o que você coloca disponível antes de perguntar*. Claude Code é fundamentalmente uma ferramenta de context engineering — o terminal, os arquivos, o CLAUDE.md, os exemplos. Tudo isso é contexto.

**Expansão para Technical AI PM:**
Como PM de produto de IA, você já pensa sobre context engineering para os seus usuários (o que você dá ao seu modelo para ele funcionar bem). Claude Code inverte isso — agora você é o usuário, e a qualidade das suas respostas depende diretamente da qualidade do contexto que você construiu no seu projeto.

Regra prática: **se o Claude deu uma resposta ruim, 80% das vezes o problema é falta de contexto, não falta de capacidade do modelo.**

---

## 2. Claude Code é um Colaborador, não um Chatbot

**O que o vídeo disse:**
> "It takes you out of the interface of just a chatbot and puts you into a file system."

**O que significa:**
Chatbot responde em texto. Claude Code age no mundo real — cria arquivos, roda código, edita documentos, instala pacotes. A diferença fundamental é **agência**.

**A implicação prática:**
Você para de pensar "vou perguntar para o Claude" e começa a pensar "vou delegar para o Claude". A pergunta muda de "o que ele vai me dizer?" para "o que ele vai fazer?".

**Expansão:**
Para um PM técnico, isso muda o fluxo de trabalho inteiro. Em vez de exportar uma análise do Claude para depois copiar no Notion, você diz "escreve isso diretamente em `strategy/okrs-q2.md`". O output já está onde precisa estar.

---

## 3. Tokens são Visíveis — e isso Muda seu Comportamento

**O que o vídeo disse:**
> "When you're using ChatGPT or Claude.ai, they never actually tell you the amount of tokens you're using. This shows the tokens counting up really fast."

**Por que importa:**
Ver os tokens te torna mais consciente do custo e da quantidade de contexto sendo processada. Quando os tokens sobem rápido = processamento pesado. Quando param = Claude está pensando ou travou.

**Regra prática derivada do vídeo:**
- Tokens subindo devagar = Claude está lendo arquivos
- Tokens subindo rápido = Claude está gerando texto
- Tokens pararam há 30s = pode estar travado (ESC e tente de novo)

**Expansão:**
Como Technical AI PM você também vai usar essa visibilidade para estimar custos de features. Se uma análise de 3 entrevistas gasta X tokens, escalar para 300 entrevistas gasta ~100X. Isso informa decisões de arquitetura do seu próprio produto.

---

## 4. A Regra do /clear

**O que o vídeo disse:**
> "Use clear a lot just to keep the context clear. It makes you much more cognizant that you are using context."

**O que a pesquisa mostra (mencionado no vídeo):**
Existe degradação de qualidade quando o contexto acumula progressivamente ao longo de uma conversa. Dar tudo de uma vez no começo é melhor do que ir adicionando aos poucos.

**Regra prática:**
```
Tarefa diferente = /clear novo
```

Não porque os arquivos somem — eles continuam lá. Mas porque a *conversa* acumulada pode confundir o Claude. Uma sessão por tipo de tarefa é o padrão ideal.

**Expansão — quando NÃO usar /clear:**
Se você está no meio de uma tarefa complexa que está indo bem, não use /clear. O histórico da conversa atual ajuda o Claude a manter coerência. /clear é para *entre* tarefas, não *dentro* de uma tarefa.

---

## 5. Claude Code vs. N8N — Duas Ferramentas Diferentes

**O que o vídeo disse:**
> "Claude Code is more tactical. N8N is for recurring automations. They're just different types of products."

**A distinção clara:**

| Claude Code | N8N / Lindy |
|---|---|
| Tarefa nova que você está fazendo agora | Tarefa recorrente que sempre acontece |
| Você está no loop, supervisionando | Roda autonomamente sem você |
| "Me ajuda a analisar essas entrevistas" | "Todo domingo, resume os posts do r/productmanagement" |
| Saída = arquivo ou resposta única | Saída = pipeline contínuo |

**Expansão para Technical AI PM:**
Isso é exatamente a distinção entre *interactive AI* e *autonomous AI* que você provavelmente já discute com seu time. Claude Code é interactive. N8N com LLM é autonomous. Conhecer os dois te dá o vocabulário certo para decidir onde colocar cada automação do seu produto.

---

## 6. Humano no Loop — a Regra de Ouro Atual

**O que o vídeo disse:**
> "We're still in this mode where there still needs to be pretty heavy human supervision. You can't go too many layers without it getting really ridiculous."

**O que isso significa na prática:**
Multi-agent systems são poderosos mas ainda frágeis. A cada agente adicionado, o risco de erro composto sobe. O vídeo recomenda: use agents para coisas que você entende bem, não para criar chains longas que você não consegue debugar.

**Expansão — a regra dos 2 níveis:**
Na prática de hoje, funciona bem com até 2 níveis de agente (orquestrador + sub-agentes). Com 3+ níveis, o erro de um agente se propaga e fica difícil de identificar onde quebrou. Para um PM, isso significa: use parallelização (1 orquestrador + N agentes iguais), evite hierarquias profundas.

---

## 7. Dê ao LLM o Trabalho que Você Odeia

**O que o vídeo disse:**
> "Have LLMs do the work you hate, not the work you love."

**Trabalho que LLMs fazem bem:**
- Transformar informação existente em novo formato
- Resumir, sintetizar, estruturar
- Pesquisar e compilar dados
- Escrever primeiros rascunhos de documentos repetitivos

**Trabalho que LLMs fazem mal:**
- Decisões estratégicas genuínas ("qual feature construir?")
- Criatividade original ("invente uma solução nova")
- Julgamento sobre pessoas e contexto político
- Qualquer coisa onde "estar errado" tem custo alto

**Expansão — a armadilha do PM:**
O vídeo menciona especificamente: "LLMs são bons em resumir user research, mas péssimos em decidir o que fazer com isso." Como PM, sua vantagem competitiva está exatamente na segunda parte. Use Claude para preparar o contexto, mas tome a decisão você mesmo.
