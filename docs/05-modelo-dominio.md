# Modelo de Domínio

## 1. Objetivo

O Modelo de Domínio apresenta os principais conceitos envolvidos no Sistema de Gestão de Eventos e Auditórios e os relacionamentos existentes entre eles.

O modelo foi elaborado com base nos requisitos funcionais, regras de negócio e casos de uso definidos na Especificação de Requisitos de Software (SRS).

---

## 2. Principais Entidades

| Entidade | Descrição |
|---|---|
| **Usuário** | Representa o usuário que acessa o sistema de forma identificada. |
| **Administrador / Organizador** | Usuário responsável pela gestão de locais, eventos, check-in e acompanhamento da operação. |
| **Participante** | Usuário que consulta eventos, realiza inscrições, acompanha sua participação e obtém certificados. |
| **Local / Auditório** | Espaço físico utilizado para realização dos eventos, possuindo identificação, capacidade e localização. |
| **Evento** | Representa um evento acadêmico cadastrado no sistema. |
| **Subevento** | Palestra, sessão ou atividade vinculada a um evento principal. |
| **Inscrição** | Representa a participação de um participante em determinado evento. |
| **Fila de Espera** | Mantém a ordem dos participantes que aguardam uma vaga em um evento lotado. |
| **Check-in** | Representa o registro da presença de um participante em um evento. |
| **Certificado** | Comprovante de participação disponibilizado aos participantes que possuem presença registrada. |

---

## 3. Diagrama do Modelo de Domínio

```mermaid
classDiagram

    class Usuario {
        credenciais
        perfil
    }

    class Administrador {
    }

    class Participante {
    }

    class Local {
        nomeIdentificacao
        capacidade
        localizacao
    }

    class Evento {
        titulo
        descricao
        data
        horarioInicio
        horarioTermino
        quantidadeVagas
        estado
    }

    class Subevento {
    }

    class Inscricao {
        situacao
    }

    class FilaEspera {
        ordemEntrada
    }

    class CheckIn {
        identificador
        dataHora
    }

    class Certificado {
        nomeParticipante
        evento
        data
        cargaHoraria
        codigoVerificacao
    }

    Usuario <|-- Administrador
    Usuario <|-- Participante

    Administrador --> Local : gerencia
    Administrador --> Evento : gerencia

    Evento --> Local : ocorre em
    Evento --> Subevento : possui

    Participante --> Inscricao : realiza
    Inscricao --> Evento : refere-se a

    Evento --> FilaEspera : pode possuir
    FilaEspera --> Inscricao : organiza

    Inscricao --> CheckIn : pode registrar

    Participante --> Certificado : recebe
    Certificado --> Evento : refere-se a
