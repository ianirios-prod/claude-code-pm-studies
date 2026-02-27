# Claude Code — Guia de Aprendizado para Technical AI PM

Este repositório captura tudo sobre **como usar Claude Code** como ferramenta de trabalho para PMs técnicos.

Criado a partir de estudo do tutorial de Claude Code + expansões práticas para o contexto de AI PM.

---

## Estrutura

```
claude-code-pm-learning/
├── CLAUDE.md                          ← Memória persistente do Claude Code
├── learning-guide/
│   ├── mental-models.md               ← 7 conceitos centrais para pensar sobre Claude Code
│   ├── tips-and-tricks.md             ← Atalhos, hacks e armadilhas para evitar
│   └── ai-tool-stack-for-pm.md        ← Stack completo de IA para Technical AI PM
└── .claude/
    └── commands/
        ├── meeting-notes.md           ← /meeting-notes
        ├── user-research.md           ← /user-research
        ├── prd.md                     ← /prd
        ├── competitive.md             ← /competitive
        ├── retro.md                   ← /retro
        ├── metrics-review.md          ← /metrics-review
        ├── experiment.md              ← /experiment
        └── feedback-synthesis.md      ← /feedback-synthesis
```

---

## O que está aqui

### `learning-guide/` — Conceitos e conhecimento

**`mental-models.md`** — Os 7 conceitos centrais do vídeo, com expansões para Technical AI PM:
- Prompt Engineering → Context Engineering
- Claude Code como colaborador (não chatbot)
- Visibilidade de tokens
- A regra do `/clear`
- Claude Code vs. N8N — quando usar cada um
- Humano no loop — a regra de ouro atual
- Dê ao LLM o trabalho que você odeia

**`tips-and-tricks.md`** — Tudo que é prático:
- Atalhos: `#`, `Shift+Tab`, `ESC`, `/clear`, `/init`
- Hacks de produtividade: CLAUDE.md em subpastas, múltiplas instâncias, input de imagens
- Stack de ferramentas ideal (Claude Pro + Cursor + N8N)
- Armadilhas para evitar (yolo mode, muitos agentes, feature ideas por LLM)

**`ai-tool-stack-for-pm.md`** — Quando usar cada ferramenta:
- Claude Code: análise, escrita, PRDs, protótipos pontuais
- N8N: automações recorrentes
- Cursor: coding pesado e exploração do codebase
- v0/Lovable: protótipos de UI rápidos

### `.claude/commands/` — Commands reutilizáveis

Templates de prompt prontos para invocar com `/nome-do-command`:

| Command | Para que serve |
|---|---|
| `/meeting-notes` | Estruturar notas de reunião + action items |
| `/user-research` | Analisar entrevista e extrair insights |
| `/prd` | Criar PRD estruturado com acceptance criteria |
| `/competitive` | Análise competitiva com matriz de features |
| `/retro` | Retrospectiva de sprint ou projeto |
| `/metrics-review` | Analisar métricas e identificar alertas |
| `/experiment` | Estruturar A/B test com hipótese e guardrails |
| `/feedback-synthesis` | Sintetizar feedback de múltiplas fontes |

---

## Repositório companion

Para **praticar** com arquivos realistas (entrevistas, PRDs, métricas, etc.):
→ `claude-code-pm-simulation` — empresa fictícia DataFlow AI como cenário de prática

---

## Como usar este repositório

### 1. Aprender os conceitos
Leia os arquivos em `learning-guide/` em ordem:
1. `mental-models.md` — entenda os princípios
2. `tips-and-tricks.md` — aprenda o que é prático
3. `ai-tool-stack-for-pm.md` — decida quando usar o quê

### 2. Usar os commands
Abra o terminal nesta pasta e rode `claude`. Os commands ficam disponíveis automaticamente.

```bash
# Exemplo: analisar uma reunião
/meeting-notes
[cole as notas brutas da reunião]
```

### 3. Adaptar para seu contexto
- Edite os commands em `.claude/commands/` para o seu produto e linguagem
- Adicione regras no `CLAUDE.md` conforme você aprende o que funciona para você

---

## Referência rápida — Atalhos essenciais

| Ação | Como |
|---|---|
| Adicionar regra ao CLAUDE.md | Comece com `#` |
| Entrar em Plan Mode | `Shift+Tab` |
| Parar o Claude | `ESC` |
| Limpar contexto | `/clear` |
| Inicializar projeto | `/init` |
