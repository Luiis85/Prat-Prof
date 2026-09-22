# Rastreabilidade

## 1. Objetivo

A rastreabilidade permite identificar a relação entre os requisitos funcionais definidos para o sistema e os casos de uso responsáveis por realizá-los.

Cada requisito funcional é relacionado a um ou mais casos de uso, permitindo verificar a cobertura das funcionalidades especificadas para o Sistema de Gestão de Eventos e Auditórios.

---

## 2. Relação entre Requisitos Funcionais e Casos de Uso

| Requisito Funcional | Casos de Uso Gerados | Justificativa |
|---|---|---|
| **RF01 — Acesso e perfis** | UC01 | O requisito de acesso identificado e distinção de perfis é realizado pela autenticação. |
| **RF02 — Gestão de locais** | UC02 | Cadastro, consulta, alteração, desativação e bloqueio de agenda concentram-se na gestão de auditórios e locais. |
| **RF03 — Disponibilidade** | UC03 (principal); UC04 (inclui) | A consulta de espaços gera UC03. A criação de evento utiliza essa consulta para atender às regras RN01 e RN02. |
| **RF04 — Gestão de eventos** | UC04 | Criação, alteração, encerramento, estados e subeventos fazem parte da gestão de eventos. |
| **RF05 — Catálogo** | UC05 | A apresentação dos eventos e de seus detalhes ao participante é realizada pelo catálogo. |
| **RF06 — Inscrição** | UC06 (principal); UC07 | A inscrição e sua confirmação são tratadas no UC06. O cancelamento previsto no requisito é tratado pelo UC07. |
| **RF07 — Fila de espera** | UC08 (principal); UC06; UC07; UC13 | O UC08 trata a entrada e a promoção da fila. UC06 direciona para a fila quando necessário; UC07 e UC13 podem provocar promoções quando uma vaga é liberada ou a quantidade de vagas aumenta. |
| **RF08 — Área do participante** | UC09 | A consulta das inscrições, dos estados e dos recursos relacionados ao check-in e certificados é realizada pela área do participante. |
| **RF09 — Check-in** | UC10 | O identificador, a validação, as rejeições e o registro da presença são realizados pelo UC10. |
| **RF10 — Certificados** | UC11; UC12 | A obtenção do certificado é realizada pelo UC11 e a verificação de autenticidade pelo UC12. |
| **RF11 — Acompanhamento administrativo** | UC13 | Consultas, contagens e ajustes administrativos relacionados aos eventos são realizados pelo UC13. |

---

## 3. Matriz RF × UC

Na matriz de rastreabilidade:

- **P** indica que o caso de uso é o principal responsável pelo requisito.
- **X** indica participação secundária do caso de uso no requisito.

| RF | UC01 | UC02 | UC03 | UC04 | UC05 | UC06 | UC07 | UC08 | UC09 | UC10 | UC11 | UC12 | UC13 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **RF01** | P | | | | | | | | | | | | |
| **RF02** | | P | | | | | | | | | | | |
| **RF03** | | | P | X | | | | | | | | | |
| **RF04** | | | | P | | | | | | | | | |
| **RF05** | | | | | P | | | | | | | | |
| **RF06** | | | | | | P | P | | | | | | |
| **RF07** | | | | | | X | X | P | | | | | X |
| **RF08** | | | | | | | | | P | | | | |
| **RF09** | | | | | | | | | | P | | | |
| **RF10** | | | | | | | | | | | P | P | |
| **RF11** | | | | | | | | | | | | | P |

---

## 4. Cobertura dos Fluxos Mínimos

| Fluxo | Casos de Uso | Requisitos Cobertos |
|---|---|---|
| **A — Planejamento de evento** | UC02, UC03, UC04 | RF02, RF03, RF04 |
| **B — Inscrição com vaga** | UC05, UC06, UC09 | RF05, RF06, RF08 |
| **C — Evento lotado e fila de espera** | UC06, UC07, UC08, UC13 | RF06, RF07, RF11 |
| **D — Presença** | UC10 | RF09 |
| **E — Certificação** | UC11, UC12 | RF10 |

---

## 5. Fluxo A — Planejamento de Evento

O fluxo de planejamento contempla:

1. Cadastro e administração dos locais.
2. Consulta de disponibilidade.
3. Criação do evento sem conflito de horário.

### Casos de Uso

- UC02 — Gerenciar auditórios e locais
- UC03 — Consultar disponibilidade de locais
- UC04 — Gerenciar eventos

### Requisitos

- RF02 — Cadastro e gestão de auditórios ou locais
- RF03 — Consulta de disponibilidade de locais
- RF04 — Cadastro e gestão de eventos

---

## 6. Fluxo B — Inscrição com Vaga

O fluxo representa uma inscrição realizada quando o evento ainda possui vagas disponíveis.

### Casos de Uso

- UC05 — Consultar catálogo e detalhes de eventos
- UC06 — Inscrever-se em evento
- UC09 — Consultar área do participante

### Requisitos

- RF05 — Catálogo e consulta de eventos
- RF06 — Inscrição em eventos
- RF08 — Área do participante

---

## 7. Fluxo C — Evento Lotado e Fila de Espera

O fluxo representa o comportamento do sistema quando um evento não possui mais vagas disponíveis.

O participante pode ingressar na fila de espera e, quando uma vaga for liberada, o sistema realiza a promoção respeitando a ordem de entrada.

### Casos de Uso

- UC06 — Inscrever-se em evento
- UC07 — Cancelar inscrição
- UC08 — Ingressar na fila de espera
- UC13 — Acompanhar operação do evento

### Requisitos

- RF06 — Inscrição em eventos
- RF07 — Fila de espera
- RF11 — Acompanhamento administrativo básico

---

## 8. Fluxo D — Presença

O fluxo representa a identificação, validação e registro da presença do participante.

Também contempla a rejeição da reutilização de um identificador já utilizado.

### Caso de Uso

- UC10 — Realizar check-in

### Requisito

- RF09 — Controle de presença / check-in

---

## 9. Fluxo E — Certificação

O fluxo representa a emissão do certificado para participantes que possuem presença registrada e a posterior verificação de sua autenticidade.

### Casos de Uso

- UC11 — Obter certificado
- UC12 — Verificar autenticidade de certificado

### Requisito

- RF10 — Certificados

---

## 10. Cobertura dos Requisitos

A matriz de rastreabilidade demonstra que todos os requisitos funcionais **RF01 a RF11** estão relacionados a pelo menos um caso de uso.

Os cinco fluxos principais do sistema também estão cobertos:

- Planejamento;
- Inscrição;
- Fila de espera;
- Presença;
- Certificação.

Dessa forma, os requisitos funcionais especificados possuem correspondência com os casos de uso responsáveis pela realização das funcionalidades do sistema.
