## 3. Requisitos Funcionais

### 3.1 Organização dos requisitos

Os requisitos funcionais foram derivados diretamente das funcionalidades F01 a F11 do documento de Visão e Escopo, reescritos no formato de RF para permitir rastreabilidade com os casos de uso. Todos possuem prioridade essencial, pois compõem o núcleo funcional do produto.

| ID | Nome | Origem | Atores |
|---|---|---|---|
| RF01 | Acesso e perfis de usuário | F01 | Administrador, Participante |
| RF02 | Cadastro e gestão de auditórios ou locais | F02 | Administrador |
| RF03 | Consulta de disponibilidade de locais | F03 | Administrador |
| RF04 | Cadastro e gestão de eventos | F04 | Administrador |
| RF05 | Catálogo e consulta de eventos | F05 | Participante |
| RF06 | Inscrição em eventos | F06 | Participante |
| RF07 | Fila de espera | F07 | Participante, Sistema |
| RF08 | Área do participante | F08 | Participante |
| RF09 | Controle de presença / check-in | F09 | Administrador, Participante |
| RF10 | Certificados | F10 | Participante, Administrador, Sistema |
| RF11 | Acompanhamento administrativo básico | F11 | Administrador |

*Tabela 1 — Catálogo dos requisitos funcionais.*

### 3.2 Especificação dos requisitos funcionais (RF01 a RF11)

#### RF01 — Acesso e perfis de usuário

| Campo | Conteúdo |
|---|---|
| Identificador | RF01 |
| Nome | Acesso e perfis de usuário |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir que os usuários acessem a solução de forma identificada, distinguir no mínimo os perfis Administrador/Organizador e Participante, e restringir as operações administrativas aos usuários autorizados. |
| Regras de negócio | — |
| Critério de aceite | Usuário autenticado visualiza apenas as operações do seu perfil; tentativa de operação administrativa por participante é recusada. |

#### RF02 — Cadastro e gestão de auditórios ou locais

| Campo | Conteúdo |
|---|---|
| Identificador | RF02 |
| Nome | Cadastro e gestão de auditórios ou locais |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir ao administrador cadastrar, consultar, alterar e desativar locais utilizados em eventos, registrando no mínimo nome/identificação, capacidade e informações de localização, bem como indisponibilidades ou bloqueios de agenda quando necessário. |
| Regras de negócio | RN01, RN02 |
| Critério de aceite | Local cadastrado fica disponível para consulta e associação a eventos; local desativado ou bloqueado não é oferecido como disponível no período correspondente. |

#### RF03 — Consulta de disponibilidade de locais

| Campo | Conteúdo |
|---|---|
| Identificador | RF03 |
| Nome | Consulta de disponibilidade de locais |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir consultar locais disponíveis para uma data e um intervalo de horário, considerando a capacidade necessária para o público esperado, retornando somente locais compatíveis e informando quando não houver local que atenda aos critérios. |
| Regras de negócio | RN01, RN02 |
| Critério de aceite | A consulta não lista locais com conflito de horário nem locais com capacidade inferior à informada; ausência de resultado é comunicada claramente. |

#### RF04 — Cadastro e gestão de eventos

| Campo | Conteúdo |
|---|---|
| Identificador | RF04 |
| Nome | Cadastro e gestão de eventos |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir criar, consultar, alterar e encerrar eventos, registrando título, descrição, data, horário de início e término, local e quantidade de vagas. Deve permitir evento principal com subeventos, apresentar estado (aberto, lotado, encerrado ou realizado) e impedir associação de eventos ao mesmo local em horários conflitantes. |
| Regras de negócio | RN01, RN02 |
| Critério de aceite | Evento é gravado com os dados obrigatórios e um estado válido; tentativa de conflito de agenda é impedida; subeventos ficam vinculados ao evento principal. |

#### RF05 — Catálogo e consulta de eventos

| Campo | Conteúdo |
|---|---|
| Identificador | RF05 |
| Nome | Catálogo e consulta de eventos |
| Prioridade | Essencial |
| Descrição | O sistema deve apresentar aos participantes os eventos disponíveis, com informações suficientes para decisão de inscrição (data, horário, local e situação das vagas), permitindo acesso aos detalhes do evento e, quando existirem, aos seus subeventos. |
| Regras de negócio | — |
| Critério de aceite | O catálogo exibe os atributos mínimos de decisão e os detalhes incluem subeventos quando houver. |

#### RF06 — Inscrição em eventos

| Campo | Conteúdo |
|---|---|
| Identificador | RF06 |
| Nome | Inscrição em eventos |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir que um participante se inscreva em um evento aberto, confirmando imediatamente a inscrição enquanto houver vagas. Deve impedir inscrições duplicadas do mesmo participante no mesmo evento, impedir novas inscrições em eventos encerrados, fechados ou já realizados, e permitir cancelamento quando aplicável. |
| Regras de negócio | RN03, RN06 |
| Critério de aceite | Com vaga disponível a inscrição é confirmada na hora; duplicidade é recusada; evento não aberto recusa inscrição; cancelamento libera a vaga. |

#### RF07 — Fila de espera

| Campo | Conteúdo |
|---|---|
| Identificador | RF07 |
| Nome | Fila de espera |
| Prioridade | Essencial |
| Descrição | Quando as vagas estiverem esgotadas, o sistema deve permitir que o participante ingresse em uma fila de espera, preservar a ordem de entrada, promover automaticamente participantes quando novas vagas forem liberadas e atualizar a situação de "em espera" para "confirmado" após a promoção. |
| Regras de negócio | RN03, RN04, RN05 |
| Critério de aceite | Evento lotado oferece fila (se habilitada); a promoção ocorre na ordem de chegada; a situação do promovido passa a confirmado. |

#### RF08 — Área do participante

| Campo | Conteúdo |
|---|---|
| Identificador | RF08 |
| Nome | Área do participante |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir que o participante consulte suas inscrições, exiba o estado de cada participação (confirmado, em fila de espera, cancelado ou concluído) e disponibilize, quando cabível, o recurso necessário para o check-in e o acesso aos certificados. |
| Regras de negócio | — |
| Critério de aceite | A área pessoal lista todas as inscrições do participante com o estado atual e atalhos de check-in/certificado quando aplicáveis. |

#### RF09 — Controle de presença / check-in

| Campo | Conteúdo |
|---|---|
| Identificador | RF09 |
| Nome | Controle de presença / check-in |
| Prioridade | Essencial |
| Descrição | O sistema deve disponibilizar, para cada inscrição confirmada, um identificador individual de check-in (QR Code ou equivalente). Quando disponível, o chip identificador do crachá do aluno deve ser a forma principal de check-in. O administrador valida o identificador no momento do evento. O check-in é aceito somente para participante inscrito no evento correspondente, não pode ser reutilizado, registra presença e horário, e informa claramente se foi aceito ou rejeitado. |
| Regras de negócio | RN07, RN08 |
| Critério de aceite | Check-in de inscrito confirmado é aceito uma única vez, com data/hora; identificador reutilizado ou participante não confirmado é rejeitado com mensagem clara. |

#### RF10 — Certificados

| Campo | Conteúdo |
|---|---|
| Identificador | RF10 |
| Nome | Certificados |
| Prioridade | Essencial |
| Descrição | O sistema deve gerar certificado de participação apenas para quem tiver presença registrada, incluindo nome do participante, evento, data e carga horária, associar um código único de verificação, permitir ao participante acessar ou obter o certificado e permitir que a organização confira a validade a partir desse código. |
| Regras de negócio | RN09, RN10 |
| Critério de aceite | Participante sem presença não recebe certificado; certificado gerado contém os dados essenciais e um código único conferível pela organização. |

#### RF11 — Acompanhamento administrativo básico

| Campo | Conteúdo |
|---|---|
| Identificador | RF11 |
| Nome | Acompanhamento administrativo básico |
| Prioridade | Essencial |
| Descrição | O sistema deve permitir ao administrador consultar eventos, inscritos e participantes presentes, apresentar contagens básicas (vagas, inscritos, pessoas em espera, presenças e certificados emitidos) e permitir ajustes administrativos necessários ao andamento do evento, como alteração da quantidade de vagas. |
| Regras de negócio | RN03, RN05 |
| Critério de aceite | Painel administrativo apresenta as contagens do evento; aumento de vagas pode promover automaticamente a fila; as consultas de inscritos e presentes estão disponíveis. |

---
