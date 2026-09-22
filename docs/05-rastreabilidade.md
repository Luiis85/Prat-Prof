## 5. Rastreabilidade

### 5.1 Relação entre requisitos funcionais e casos de uso

Cada requisito funcional do catálogo originou um ou mais casos de uso. A tabela a seguir registra a rastreabilidade de origem (qual RF gerou quais UC), distinguindo o caso de uso principal daqueles que apenas consomem o requisito em um fluxo específico.

| Requisito funcional | Casos de uso gerados | Justificativa da derivação |
|---|---|---|
| RF01 — Acesso e perfis | UC01 | O requisito de acesso identificado e distinção de perfis é realizado integralmente pela autenticação. |
| RF02 — Gestão de locais | UC02 | Cadastro, consulta, alteração, desativação e bloqueio de agenda concentram-se na gestão de auditórios. |
| RF03 — Disponibilidade | UC03 (principal); UC04 (inclui) | A consulta avulsa de espaços gera UC03. A criação de evento inclui essa consulta para cumprir RN01/RN02. |
| RF04 — Gestão de eventos | UC04 | Criação, alteração, encerramento, estados e subeventos são o núcleo de UC04. |
| RF05 — Catálogo | UC05 | A apresentação de eventos e detalhes ao participante origina o catálogo. |
| RF06 — Inscrição | UC06 (principal); UC07 | Confirmação de vaga e impedimentos geram UC06. O cancelamento previsto no mesmo RF gera UC07. |
| RF07 — Fila de espera | UC08 (principal); UC06 (estende); UC07; UC13 | A entrada e a promoção da fila geram UC08. UC06 encaminha à fila; UC07 e UC13 disparam promoção ao liberar ou aumentar vagas. |
| RF08 — Área do participante | UC09 | Consulta de inscrições, estados, check-in e certificados na visão do participante geram UC09. |
| RF09 — Check-in | UC10 | Identificador, validação, rejeições e registro de presença/horário geram UC10. |
| RF10 — Certificados | UC11 (emissão); UC12 (verificação) | A geração/obtenção pelo participante gera UC11. A conferência do código pela organização gera UC12. |
| RF11 — Acompanhamento admin. | UC13 | Consultas, contagens e ajuste de vagas geram o acompanhamento operacional. |

*Tabela 3 — Rastreabilidade de origem: quais RF geraram quais UC.*

### 5.2 Matriz RF × UC

Na matriz, "P" indica caso de uso principal derivado do requisito e "X" indica participação secundária (include, extend ou disparo de regra).

| RF | UC01 | UC02 | UC03 | UC04 | UC05 | UC06 | UC07 | UC08 | UC09 | UC10 | UC11 | UC12 | UC13 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RF01 | P | | | | | | | | | | | | |
| RF02 | | P | | | | | | | | | | | |
| RF03 | | | P | X | | | | | | | | | |
| RF04 | | | | P | | | | | | | | | |
| RF05 | | | | | P | | | | | | | | |
| RF06 | | | | | | P | P | | | | | | |
| RF07 | | | | | | X | X | P | | | | | X |
| RF08 | | | | | | | | | P | | | | |
| RF09 | | | | | | | | | | P | | | |
| RF10 | | | | | | | | | | | P | P | |
| RF11 | | | | | | | | | | | | | P |

*Tabela 4 — Matriz de rastreabilidade RF × UC (P = principal; X = secundário).*

### 5.3 Cobertura dos fluxos mínimos do documento de visão

| Fluxo mínimo (Visão e Escopo) | Casos de uso que o realizam | Requisitos cobertos |
|---|---|---|
| A — Planejamento de evento (cadastrar local, consultar disponibilidade, criar evento sem conflito) | UC02, UC03, UC04 | RF02, RF03, RF04 |
| B — Inscrição com vaga (catálogo, inscrição confirmada, área pessoal) | UC05, UC06, UC09 | RF05, RF06, RF08 |
| C — Evento lotado e fila de espera (ingresso e promoção automática) | UC06, UC07, UC08, UC13 | RF06, RF07, RF11 |
| D — Presença (identificador, validação e registro, com rejeição de reuso) | UC10 | RF09 |
| E — Certificação (emissão com código único e conferência pela organização) | UC11, UC12 | RF10 |

*Tabela 5 — Cobertura dos fluxos mínimos A a E.*

A matriz e as tabelas de origem demonstram cobertura completa dos requisitos funcionais F01–F11 / RF01–RF11 por pelo menos um caso de uso, e cobertura dos cinco fluxos mínimos exigidos pelo documento de Visão e Escopo.
