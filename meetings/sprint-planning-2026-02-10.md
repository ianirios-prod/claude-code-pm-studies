# Sprint Planning — Sprint 42
**Data:** 2026-02-10
**Participantes:** PM (você), Bruno Carvalho (Eng Lead), Camila Torres (Designer), Priya Sharma (Data Scientist)
**Duração:** 1h30

---

## Transcrição

**PM:** Pessoal, sprint 42. Vamos focar no AI Insights Feed. Rafael quer uma demo pra semana que vem com clientes Enterprise. Quais são as histórias que conseguimos fechar?

**Bruno:** Tenho minhas reservas sobre o prazo. A latência ainda está em 4.2 segundos. Se a gente mostrar isso pro cliente, vai ser constrangedor. Precisamos de pelo menos mais uma sprint pra otimizar antes de demo.

**PM:** Entendo, mas o compromisso com o Rafael foi para essa sprint. O que conseguimos fazer pra melhorar a latência sem atrasar o resto?

**Bruno:** Posso paralelizar as chamadas de LLM. Hoje é tudo sequencial. Se fizermos paralelo, a gente provavelmente chega em 2.5–3 segundos. Não é os 2 segundos que a gente quer, mas é aceitável pra demo.

**Priya S.:** Eu precisaria de 2 dias pra ajustar o prompt do insight pra incluir o contexto que as entrevistas mostraram que falta. Ana e Priya Chen reclamaram exatamente disso.

**Camila:** O wireframe do feed tá pronto. Precisamos decidir se vai ter card de "por que esse insight apareceu" ou deixamos pra depois.

**PM:** Priya Chen pediu exatamente isso. Vamos colocar uma versão simplificada agora — só mostrar as 2 métricas que geraram o insight, sem o raciocínio completo. O raciocínio completo fica como tech debt pra sprint 43.

**Bruno:** Concordo. Assim consigo entregar o parallelization + o card básico em uma sprint.

**Camila:** Vou ajustar o design pra incluir o card simplificado. Mais 1 dia de design.

**PM:** Combinado. Histórias da sprint:
1. Parallelização das chamadas de LLM (Bruno, 5 dias)
2. Atualização do prompt de insights com contexto (Priya S., 2 dias)
3. Card "por que esse insight" — versão simplificada (Camila design, Bruno dev, 3 dias)
4. Integração Slack — notificação proativa (Bruno, 3 dias)
5. Testes de performance e QA (todos, 2 dias)

**Bruno:** A história 4 é ambiciosa. Se der problema na latência, essa pode ser cortada.

**PM:** Anotado. Prioridade: 1, 2, 3 são must-haves. 4 é nice-to-have pra sprint.

---

## Action Items
| Responsável | Ação | Prazo |
|---|---|---|
| Bruno | Implementar parallelização de LLM calls | 2026-02-13 |
| Priya S. | Atualizar prompt com contexto de negócio | 2026-02-12 |
| Camila | Wireframe do card "por que esse insight" | 2026-02-11 |
| PM | Confirmar escopo da demo com Rafael | 2026-02-11 |
| PM | Criar ticket de tech debt para raciocínio completo | 2026-02-11 |

## Riscos
- **Latência:** Parallelização pode não ser suficiente — plano B é fazer demo offline/pré-carregada
- **Prazo:** 5 histórias em 1 sprint é apertado — Bruno pode precisar de ajuda de outro engenheiro
