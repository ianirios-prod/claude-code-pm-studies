# Tips & Tricks — Tudo que o Vídeo Mostrou (+ Expansões)

---

## Atalhos e Comandos Essenciais

### `#` — Adicionar regra ao CLAUDE.md instantaneamente
**Do vídeo:** Digitar `#` seguido de uma regra adiciona automaticamente ao project memory.
```
# sempre usar markdown nos outputs
# nunca criar arquivos fora das pastas do projeto
# quando pesquisar na web, sempre incluir as fontes
```
**Quando usar:** Sempre que Claude fizer algo que você não gostou e quiser que nunca mais aconteça.

---

### `Shift+Tab` — Alternar Plan Mode
**Do vídeo:** Plan Mode impede o Claude de editar arquivos. Ele só lê, pesquisa e planeja.
**Quando usar:** Qualquer tarefa que envolva múltiplos arquivos ou decisões que você quer revisar antes de executar.
**Expansão:** Use Plan Mode especialmente quando:
- O output errado seria difícil de reverter
- A tarefa tem dependências (fazer A antes de B)
- Você não tem certeza do escopo

---

### `ESC` — Parar o Claude imediatamente
**Do vídeo:** "You can always exit by just hitting the escape command."
**Quando usar:** Claude começou a fazer algo errado, está em loop, ou você mudou de ideia sobre a tarefa.

---

### `/clear` — Resetar contexto da conversa
**Do vídeo:** Usado frequentemente para manter contexto limpo entre tarefas.
**O que faz:** Apaga o histórico da conversa atual. Os arquivos continuam intactos.
**Quando NÃO usar:** No meio de uma tarefa que está indo bem.

---

### `/init` — Inicializar projeto
**Do vídeo:** Analisa toda a estrutura de pastas e cria/atualiza o CLAUDE.md automaticamente.
**Quando usar:** Ao abrir um projeto pela primeira vez, ou quando a estrutura mudou muito.
**O que gera:** Um CLAUDE.md com a estrutura do projeto, componentes principais e como tudo se conecta.

---

## Hacks de Produtividade

### CLAUDE.md em Subpastas
**Do vídeo:** "You can put CLAUDE.md files into subfolders and anytime it's doing something in those subfolders, it will follow those rules."
**Exemplo prático:**
```
prds/CLAUDE.md  → "Sempre incluir acceptance criteria com critérios mensuráveis. Nunca aprovar PRD sem Non-Goals explícitos."
meetings/CLAUDE.md → "Sempre gerar action items com dono e prazo. Formato de data: DD/MM/YYYY."
```
**Por que é poderoso:** Regras específicas por contexto, sem poluir o CLAUDE.md principal.

---

### Múltiplas Instâncias Simultâneas
**Do vídeo:** "I've heard there are engineers who run 6 instances of Claude Code at the same time."
**Como fazer:** Abrir múltiplos terminais, digitar `claude` em cada um.
**Caso de uso para PM:**
- Terminal 1: Processando análise de user research (tarefa longa)
- Terminal 2: Rascunhando email para stakeholder enquanto espera
- Terminal 3: Pesquisando competidor

---

### GitHub Repos como Input Direto
**Do vídeo:** "You can bring in any code that you find on GitHub and Claude Code can just use it right away."
**Como usar:** Cole o link do repositório e peça para o Claude usar aquela biblioteca/API.
**Caso de uso para PM técnico:** Encontrou um SDK de analytics interessante no GitHub? Cole o link e peça para o Claude criar um script de prova de conceito.

---

### Imagens e Screenshots Direto no Terminal
**Do vídeo:** Arrastar imagem para o terminal funciona. Screenshots também.
**Casos de uso para PM:**
- Screenshot de dashboard do competidor → "Analise esse UI e compare com o nosso"
- Screenshot de bug reportado pelo usuário → "O que pode estar causando isso?"
- Print de métrica do Amplitude → "Que insights você tira desse gráfico?"

---

### Whisper Flow — Ditado por Voz
**Do vídeo:** "I'm using a tool called Whisper Flow to help me just dictate commands because it's a little bit faster, which I highly recommend."
**O que é:** Ferramenta que transcreve sua voz em texto em tempo real no terminal.
**Por que vale:** Para tarefas longas de PM (ex: "analise as 3 entrevistas, cruze com os OKRs, e escreva um rascunho de PRD"), digitar o prompt todo é tedioso. Falar é 3-5x mais rápido.

---

## Stack de Ferramentas Ideal (segundo o vídeo)

O Carl recomendou explicitamente essa combinação:

| Ferramenta | Uso | Custo |
|---|---|---|
| **Claude Pro** | Tudo que é text-based: research, PRDs, análises, meetings | $17/mês |
| **Cursor** | Coding pesado que precisa de Opus | $20/mês |
| **N8N** | Automações recorrentes (monitoring, digests) | Grátis (self-hosted) ou $20/mês |
| **Total** | Stack completo de PM técnico | ~$37-57/mês |

**Por que Claude Pro + Cursor em vez de Claude Max?**
Claude Max custa $100+/mês. Claude Pro ($17) + Cursor ($20) dá acesso ao Sonnet para PM work + modelos premium para coding, por menos dinheiro. Para PMs que não estão codando pesado o tempo todo, essa combinação tem melhor ROI.

---

## Armadilhas para Evitar

### Armadilha 1: Yolo Mode sem Cuidado
**Do vídeo:** Existe um modo onde Claude faz tudo sem pedir permissão.
**Cuidado:** "We're literally having it work with the files on your computer. You have to be very careful, especially if you're doing code-based stuff."
**Regra:** Só use yolo mode em pastas de aprendizado/teste, nunca em projetos com dados reais importantes.

### Armadilha 2: Muitos Agentes em Cadeia
**Do vídeo:** Mais agentes = mais risco de output ruim e difícil de debugar.
**Regra:** Para PM, prefira 1 agente paralelo repetido (analisar 5 entrevistas em paralelo) a 5 agentes em sequência (um resume, o outro analisa, o outro prioriza...).

### Armadilha 3: Pedir Feature Ideas para o LLM
**Do vídeo:** "An LLM agent that comes up with feature ideas — I would be very skeptical."
**Expansão:** LLMs são bons em *sintetizar* o que os usuários disseram. São ruins em *decidir* o que construir. Use Claude para preparar o material de decisão, não para tomar a decisão.

### Armadilha 4: Apresentar Protótipo como Código de Produção
**Do vídeo:** "Don't present it as production-ready. Present it as 'here's an idea — of course we need to figure out how to actually build it'."
**Para PM:** O protótipo do Claude é uma ferramenta de comunicação com engenharia, não um entregável. Use para alinhar visão, identificar edge cases que você não pensaria só no Figma.

### Armadilha 5: Contexto Acumulando sem /clear
**Do vídeo:** Degradação de qualidade quando o contexto acumula progressivamente.
**Sinal de alerta:** Claude começou a dar respostas estranhas ou inconsistentes → provavelmente é contexto velho interferindo → use /clear.

---

## Base de Agentes Pré-Prontos

**Do vídeo:** Existe uma base chamada `subagents.cc` com agentes prontos para importar.

**Como usar:**
```
# No Claude Code:
"Vá em subagents.cc, encontre um agente de legal review para produtos de software e instale no projeto."
```

**Agentes úteis para PM técnico (para buscar):**
- Legal advisor — revisa PRDs antes de ir para legal
- Security reviewer — aponta vulnerabilidades em specs técnicas
- Data privacy reviewer — identifica riscos de LGPD/GDPR
- Accessibility reviewer — verifica se specs consideram acessibilidade
