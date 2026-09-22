# Wireframes da Interface

## 1. Objetivo

Os wireframes representam a interface em baixa fidelidade do Sistema de Gestão de Eventos e Auditórios.

Eles não definem uma tecnologia específica de implementação, servindo apenas para representar visualmente os casos de uso, os fluxos do sistema e as regras de negócio descritas na Especificação de Requisitos de Software.

---

## 2. Relação entre Wireframes e Casos de Uso

| Wireframe | Tela | Casos de Uso | Função na Interface |
|---|---|---|---|
| **WF00** | Mapa de telas | UC01–UC13 | Visão geral do fluxo entre as telas e cobertura dos fluxos A–E. |
| **WF01** | Autenticação | UC01 | Login identificado e restrição por perfil. |
| **WF02** | Locais | UC02 | Cadastro, consulta, alteração, desativação e bloqueios de auditórios ou locais. |
| **WF03** | Disponibilidade e evento | UC03, UC04 | Busca de espaço compatível e cadastro do evento. |
| **WF04** | Catálogo e inscrição | UC05, UC06, UC08 | Consulta de eventos, inscrição confirmada e fila de espera. |
| **WF05** | Área do participante | UC07, UC08, UC09 | Inscrições, estados, identificação para check-in e cancelamento. |
| **WF06** | Check-in | UC10 | Validação de presença por crachá, QR Code ou mecanismo equivalente. |
| **WF07** | Certificados | UC11, UC12 | Obtenção do certificado pelo participante e verificação pela organização. |
| **WF08** | Painel administrativo | UC13 | Contagens, participantes presentes e ajuste da quantidade de vagas. |

---

## 3. WF00 — Mapa de Telas

O mapa de telas apresenta o encadeamento geral das interfaces do sistema e demonstra a cobertura dos principais fluxos funcionais.

<img width="1065" height="658" alt="00" src="https://github.com/user-attachments/assets/2f8e1b72-b9dd-4b76-bfc8-02e755d592e2" />

---

## 4. WF01 — Autenticação

O wireframe de autenticação representa o acesso identificado ao sistema.

Está relacionado ao:

- **UC01 — Autenticar usuário**

O sistema identifica o perfil do usuário e disponibiliza somente as operações permitidas para Administrador/Organizador ou Participante.

<img width="975" height="623" alt="0" src="https://github.com/user-attachments/assets/e9b098b4-23a3-4757-82b8-f756f8135bfb" />


---

## 5. WF02 — Gestão de Auditórios e Locais

O wireframe apresenta as funcionalidades relacionadas ao cadastro e gerenciamento dos locais utilizados para realização dos eventos.

Está relacionado ao:

- **UC02 — Gerenciar auditórios e locais**

Permite representar operações como:

- cadastro de local;
- consulta;
- alteração;
- desativação;
- capacidade;
- localização;
- bloqueios ou indisponibilidades.

<img width="994" height="622" alt="02" src="https://github.com/user-attachments/assets/b6d10f78-6607-40b2-b40f-d92d73632ee7" />


---

## 6. WF03 — Disponibilidade e Cadastro de Evento

O wireframe representa a consulta de disponibilidade dos locais e o cadastro de eventos.

Está relacionado aos casos de uso:

- **UC03 — Consultar disponibilidade de locais**
- **UC04 — Gerenciar eventos**

O fluxo considera a disponibilidade do local, o horário e a capacidade necessária antes da criação do evento.

<img width="993" height="636" alt="03" src="https://github.com/user-attachments/assets/340028f9-152b-4943-b74d-629b18b99dc5" />


---

## 7. WF04 — Catálogo, Inscrição e Fila de Espera

O wireframe representa o catálogo de eventos disponível para o participante e o processo de inscrição.

Está relacionado aos casos de uso:

- **UC05 — Consultar catálogo e detalhes de eventos**
- **UC06 — Inscrever-se em evento**
- **UC08 — Ingressar na fila de espera**

Quando houver vagas, a inscrição pode ser confirmada.

Quando o evento estiver lotado e a fila estiver habilitada, o participante poderá ingressar na fila de espera.

<img width="991" height="598" alt="04" src="https://github.com/user-attachments/assets/b430fe0e-78ea-494d-b60e-0dcd3cf367e8" />

---

## 8. WF05 — Área do Participante

O wireframe representa a área pessoal do participante.

Está relacionado aos casos de uso:

- **UC07 — Cancelar inscrição**
- **UC08 — Ingressar na fila de espera**
- **UC09 — Consultar área do participante**

A interface apresenta as inscrições e seus respectivos estados, como:

- confirmado;
- em fila de espera;
- cancelado;
- concluído.

Também permite acesso aos recursos relacionados ao check-in e aos certificados quando aplicável.

<img width="993" height="635" alt="05" src="https://github.com/user-attachments/assets/b57d0815-3627-4f96-baa6-7f1d0f1c7364" />


---

## 9. WF06 — Check-in

O wireframe representa o processo de validação e registro da presença do participante.

Está relacionado ao:

- **UC10 — Realizar check-in**

O participante apresenta seu identificador, que pode ser:

- chip do crachá;
- QR Code;
- mecanismo equivalente.

O sistema valida a inscrição e registra a presença e o horário quando o check-in for aceito.

<img width="993" height="591" alt="06" src="https://github.com/user-attachments/assets/a3f367a7-babb-4f02-a03a-40a24ff8a2b0" />


---

## 10. WF07 — Certificados

O wireframe representa o acesso e a verificação dos certificados de participação.

Está relacionado aos casos de uso:

- **UC11 — Obter certificado**
- **UC12 — Verificar autenticidade de certificado**

O participante com presença registrada pode obter seu certificado.

A organização pode verificar sua autenticidade utilizando o código único de verificação.

<img width="992" height="631" alt="07" src="https://github.com/user-attachments/assets/014bd86f-5b11-42a5-b09d-ad52091d2f87" />


---

## 11. WF08 — Painel Administrativo

O wireframe representa o acompanhamento operacional dos eventos pelo Administrador/Organizador.

Está relacionado ao:

- **UC13 — Acompanhar operação do evento**

A interface apresenta informações como:

- quantidade de vagas;
- inscritos;
- participantes em espera;
- presenças;
- certificados emitidos.

Também permite o ajuste administrativo da quantidade de vagas.

<img width="998" height="636" alt="08" src="https://github.com/user-attachments/assets/2ad54630-9a15-4c5a-8cc6-b0375c187f83" />


---

## 12. Correspondência com os Fluxos do Sistema

### Fluxo A — Planejamento

**Locais → Disponibilidade → Eventos**

Relaciona o cadastro de locais, a consulta de disponibilidade e a criação do evento.

---

### Fluxo B — Inscrição com Vaga

**Catálogo → Inscrição → Área do Participante**

O participante consulta o evento, realiza a inscrição e acompanha sua situação na área pessoal.

---

### Fluxo C — Fila de Espera

**Catálogo → Fila de Espera → Promoção Automática**

Quando o evento estiver lotado, o participante pode entrar na fila de espera.

Quando uma vaga for liberada, o próximo participante elegível poderá ser promovido para uma inscrição confirmada.

---

### Fluxo D — Presença

**Área do Participante → Identificação → Check-in**

O participante apresenta seu identificador e o Administrador/Organizador realiza a validação da presença.

---

### Fluxo E — Certificação

**Presença → Certificado → Verificação**

Após a presença registrada, o participante pode obter o certificado e sua autenticidade pode ser conferida por meio do código de verificação.
