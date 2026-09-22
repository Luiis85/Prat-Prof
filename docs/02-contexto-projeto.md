## 2. Contexto do Projeto

### 2.1 Problema e motivação

Instituições de ensino realizam palestras, seminários, semanas acadêmicas e outros eventos que exigem coordenação de espaços, horários, vagas, inscrições, presença e certificação. Quando essas atividades são tratadas por ferramentas desconectadas ou por procedimentos manuais, a organização tende a enfrentar conflitos de agenda, dificuldade para controlar lotação e filas de espera, registro de presença pouco confiável e maior esforço para emissão de certificados.

O projeto propõe uma solução integrada para apoiar o ciclo operacional de eventos acadêmicos, desde o planejamento do evento e a reserva do auditório até a inscrição dos participantes, o controle de presença e a disponibilização de certificados.

### 2.2 Declaração de visão

Para organizadores e participantes de eventos acadêmicos que precisam administrar espaços, vagas e participação de forma coordenada, o Sistema de Gestão de Eventos e Auditórios é uma plataforma que centraliza a criação de eventos, a alocação de auditórios, as inscrições, o controle de presença e a certificação. Diferentemente de um conjunto de controles manuais ou de ferramentas isoladas, a solução mantém essas atividades relacionadas em um fluxo único e consistente.

### 2.3 Objetivos

- Reduzir o esforço operacional necessário para organizar eventos acadêmicos.
- Evitar conflitos de uso de auditórios e apoiar a escolha de espaços compatíveis com a quantidade esperada de participantes.
- Controlar automaticamente a quantidade de vagas disponíveis e o tratamento de eventos lotados.
- Dar ao participante uma visão clara de suas inscrições e de sua situação em cada evento.
- Registrar a presença dos participantes de forma rápida e auditável.
- Automatizar a emissão de certificados para participantes que efetivamente compareceram ao evento.
- Permitir que organizadores acompanhem informações básicas sobre eventos, inscrições, presença e certificação.

### 2.4 Perfis de usuário

| Perfil | Responsabilidades e necessidades principais |
|---|---|
| Administrador / Organizador | Cadastra e administra auditórios; cria e gerencia eventos; consulta disponibilidade de espaços; acompanha vagas e inscrições; realiza o check-in; acompanha presenças e certificados. |
| Participante | Consulta eventos; realiza e cancela inscrições; acompanha inscrição confirmada ou fila de espera; apresenta sua identificação de check-in; consulta e obtém seus certificados. |

### 2.5 Perspectiva do produto

A solução deve ser entendida como um sistema de apoio à gestão do ciclo de eventos. A forma de implementação é deliberadamente aberta: a equipe poderá decidir como estruturar a aplicação e em quais plataformas disponibilizá-la, desde que os fluxos funcionais e as regras de negócio essenciais descritos neste documento sejam preservados.

### 2.6 Escopo funcional e itens fora de escopo

Estão no escopo as funcionalidades de acesso e perfis, gestão de auditórios, consulta de disponibilidade, gestão de eventos, catálogo, inscrição, fila de espera, área do participante, check-in, certificados e acompanhamento administrativo básico.

Não são obrigatórios, podendo ser tratados apenas como extensões:

- Notificações automáticas por e-mail, SMS ou push.
- Relatórios analíticos avançados, dashboards históricos, gráficos e exportação em múltiplos formatos.
- Portal público automatizado para validação de certificados por terceiros — basta existir mecanismo de conferência do código pela organização.
- Integrações com sistemas acadêmicos.
- Recursos financeiros, venda de ingressos, pagamentos ou cobrança de inscrições.

### 2.7 Regras de negócio essenciais

| ID | Descrição |
|---|---|
| RN01 | Um local não pode receber dois eventos com horários sobrepostos. |
| RN02 | A capacidade de um local deve ser considerada na escolha do espaço para o evento. |
| RN03 | O número de inscrições confirmadas não deve ultrapassar a quantidade de vagas definida para o evento. |
| RN04 | Quando não houver vagas, novas solicitações devem ser encaminhadas para a fila de espera, se ela estiver habilitada. |
| RN05 | A promoção da fila de espera deve respeitar a ordem de entrada. |
| RN06 | Um participante não pode possuir mais de uma inscrição ativa no mesmo evento. |
| RN07 | Somente inscrições confirmadas podem resultar em check-in válido. |
| RN08 | Um check-in já registrado não pode ser contabilizado novamente. |
| RN09 | Somente participantes com presença registrada podem receber certificado. |
| RN10 | Cada certificado deve possuir um identificador único que permita sua conferência posterior. |

### 2.8 Premissas, dependências e restrições

- **Premissa:** usuários possuem identificação institucional, e o chip do crachá do aluno pode ser usado como forma principal de check-in quando disponível.
- **Premissa:** cada inscrição confirmada possui um identificador individual de check-in, apresentado como QR Code ou mecanismo equivalente.
- **Dependência:** o documento de Visão e Escopo é a fonte dos fluxos mínimos (planejamento, inscrição, fila, presença e certificação).
- **Restrição:** operações administrativas ficam restritas a usuários autorizados do perfil Administrador/Organizador.
- **Restrição de design:** a arquitetura e a plataforma não são impostas por esta SRS, desde que os requisitos funcionais e as regras de negócio sejam atendidos.

---
