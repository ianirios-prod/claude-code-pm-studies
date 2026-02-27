# Claude Code — Projeto de Aprendizado para Technical AI PM

Este projeto foi criado para você praticar todas as funcionalidades do Claude Code com exemplos reais de Product Management.

**Empresa fictícia:** DataFlow AI — plataforma de analytics com IA para times de produto
**Seu papel:** Technical AI PM

---

## Estrutura do Projeto

```
claude-code-pm-learning/
├── CLAUDE.md                          ← Memória persistente (lida em toda sessão)
├── context/
│   ├── business-info.md               ← Contexto da empresa para prompts
│   └── writing-styles.md              ← Estilos de escrita por audiência
├── user-research/
│   ├── interview-ana-martins.md       ← Head of Product, fintech
│   ├── interview-joao-silva.md        ← PM solo, e-commerce (risco de churn)
│   └── interview-priya-chen.md        ← VP of Product, Enterprise
├── meetings/
│   ├── sprint-planning-2026-02-10.md
│   ├── stakeholder-review-2026-02-17.md
│   └── engineering-sync-2026-02-20.md
├── prds/
│   └── prd-example-ai-insights.md    ← Template de PRD
└── .claude/
    └── commands/
        ├── meeting-notes.md           ← /meeting-notes
        ├── user-research.md           ← /user-research
        ├── prd.md                     ← /prd
        ├── competitive.md             ← /competitive
        └── retro.md                   ← /retro
```

---

## Plano de Aprendizado — 10 Funcionalidades

### 1. Setup + CLAUDE.md (Memória Persistente)
**O que é:** Arquivo que o Claude lê no início de toda sessão — seu contexto permanente.
**Pratique:**
```
# Abra este projeto no terminal e rode:
claude

# Teste se o Claude "sabe" seu contexto:
"Qual é o maior problema que nossos usuários relataram sobre o AI Insights?"
"Quem é o Eng Lead do meu time?"
```
**Por que importa para PMs:** Nunca mais precisar repetir "trabalho numa empresa de analytics B2B..." em todo prompt.

---

### 2. Leitura e Análise de Arquivos
**O que é:** Claude lê arquivos da sua pasta e analisa o conteúdo.
**Pratique:**
```
"Quantas entrevistas de usuário temos e quais são os perfis?"
"Qual usuário tem maior risco de churn? Por que?"
"Compare as dores da Ana Martins com as da Priya Chen — o que têm em comum?"
```
**Por que importa:** Análise de user research em segundos, sem copiar/colar manualmente.

---

### 3. Web Search Integrada
**O que é:** Claude busca informações atualizadas na web diretamente.
**Pratique:**
```
"Pesquise como o Mixpanel e o Amplitude abordam personalização de insights por objetivo. Me dê um resumo com fontes."
"O que há de mais recente sobre LLM evaluation frameworks para produtos de AI? Foco em 2025-2026."
"Pesquise o pricing atual do PostHog e compare com o nosso."
```
**Por que importa:** Pesquisa competitiva sem sair do terminal.

---

### 4. Custom Commands (Slash Commands)
**O que é:** Prompts salvos que você aciona com `/nome-do-comando`.
**Pratique:**
```
/meeting-notes meetings/engineering-sync-2026-02-20.md

/user-research user-research/

/prd "Feature: Webhook API para integração com dashboards externos"

/retro meetings/
```
**Por que importa:** Seus melhores prompts viram ferramentas reutilizáveis. Um `/prd` sempre produz PRDs no seu formato.

---

### 5. Plan Mode (Shift+Tab)
**O que é:** Modo onde o Claude planeja sem executar — você revisa o plano antes de aprovar.
**Pratique:**
```
# Ative Plan Mode com Shift+Tab, depois:
"Quero criar um relatório executivo consolidando as 3 entrevistas de usuário,
o sprint planning e o stakeholder review para apresentar ao board.
Planeje como você faria isso."

# Revise o plano, corrija se necessário, depois saia do Plan Mode
```
**Por que importa:** Para tarefas complexas com múltiplos arquivos, ver o plano evita retrabalho.

---

### 6. Sub-agentes em Paralelo
**O que é:** Claude cria instâncias paralelas para processar tarefas simultaneamente.
**Pratique:**
```
"Analise cada entrevista de usuário em paralelo e para cada uma gere:
1. Top 3 dores
2. Risco de churn (alto/médio/baixo + justificativa)
3. Uma feature request prioritária
Processe as 3 entrevistas ao mesmo tempo."
```
**Por que importa:** O que levaria 3 prompts sequenciais acontece em 1 (3x mais rápido para grandes volumes).

---

### 7. Agentes Customizados
**O que é:** Personas com contexto específico que revisam trabalho de diferentes perspectivas.
**Pratique:** Crie um arquivo `.claude/agents/cto-reviewer.md`:
```markdown
---
name: CTO Reviewer
color: red
description: Reviews product decisions from a technical and scalability perspective
---
You are Rafael Mendes, CTO da DataFlow AI. Você é técnico, direto, obcecado com performance e escalabilidade.
Quando revisar um PRD ou decisão, foque em: viabilidade técnica, riscos de escalabilidade, tech debt,
custo de infraestrutura. Seja cético. Faça perguntas difíceis.
```
Depois:
```
"Revise o PRD de AI Insights Personalization do ponto de vista do CTO Rafael,
do Designer Camila e de um cliente Enterprise cético."
```
**Por que importa:** Obtenha feedback de múltiplas perspectivas sem precisar de reunião.

---

### 8. MCPs (Model Context Protocol)
**O que é:** Ferramentas externas que você conecta ao Claude Code.
**MCPs úteis para PMs:**
- **Slack MCP:** Rascunha e envia mensagens direto do terminal
- **GitHub MCP:** Cria issues, PRs, lê código
- **Google Drive MCP:** Acessa docs e sheets do Drive
- **Linear/Jira MCP:** Cria e atualiza tickets

**Para instalar um MCP:**
```bash
# Exemplo com Slack (substitua pelo seu token)
claude mcp add slack -- npx -y @modelcontextprotocol/server-slack

# Depois no Claude Code:
"Redija uma mensagem no Slack para o canal #product-team resumindo os principais riscos
identificados no engineering sync de hoje."
```

---

### 9. Execução de Código
**O que é:** Claude escreve e executa código para você — análises, automações, scripts.
**Pratique:**
```
"Escreva um script Python que leia todas as entrevistas de usuário nesta pasta
e gere um CSV com: nome, empresa, plano, top 3 dores, risco de churn."

"Crie um script que monitore um arquivo de métricas e me avise quando DAU
cair mais de 5% em relação à média dos últimos 7 dias."
```
**Por que importa:** Automatize análises repetitivas sem precisar de data scientist para cada script.

---

### 10. Prototipagem Rápida
**O que é:** Claude gera código de protótipos funcionais direto no terminal.
**Pratique:**
```
# Entre em Plan Mode primeiro (Shift+Tab), depois:
"Crie um protótipo HTML/CSS/JS simples do AI Insights Feed com:
- Lista de insights com badge de relevância por objetivo
- Card expandível com 'por que esse insight apareceu'
- Filtro por objetivo (churn, ativação, DAU)
Use dados mockados das entrevistas que temos no projeto."
```
**Por que importa:** Valide UX com stakeholders antes de envolver engenharia.

---

## Exercícios Avançados (combine features)

### Exercício A — Pipeline Completo de User Research
```
1. /user-research user-research/
2. "Com base nessa síntese, escreva um one-pager executivo para o Rafael
   justificando priorizar o eval pipeline antes da personalização por OKR.
   Use o estilo 'executivos' de context/writing-styles.md"
```

### Exercício B — Prep de Sprint Planning
```
1. "Analise em paralelo: as 3 entrevistas de usuário, o stakeholder review e
   o engineering sync. Gere uma lista priorizada de histórias para o sprint 43
   com justificativa baseada em evidências de cada arquivo."
```

### Exercício C — Análise Competitiva + PRD
```
1. /competitive "personalização de insights por objetivo em analytics de produto"
2. "Com base na análise competitiva e nas entrevistas de usuário, escreva o PRD
   completo para a feature de personalização por OKR usando /prd"
```

---

## Dicas Rápidas

| Situação | O que fazer |
|---|---|
| Claude começou a fazer algo errado | Pressione ESC para parar |
| Contexto da conversa está confuso | `/clear` para resetar |
| Quer que lembre uma regra sempre | `#regra aqui` para adicionar ao CLAUDE.md |
| Tarefa complexa com múltiplos arquivos | Use Plan Mode (Shift+Tab) primeiro |
| Tokens acabando | `/clear` e comece nova sessão com contexto específico |
| Claude cometeu erro num arquivo | Use `git diff` para ver o que mudou antes de aprovar |
