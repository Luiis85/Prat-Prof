## 1. Introdução

### 1.1 Finalidade

Este documento apresenta a Especificação de Requisitos de Software (SRS) do Sistema de Gestão de Eventos e Auditórios. O objetivo é descrever o comportamento externo da solução de forma suficiente para orientar análise, projeto, implementação e testes, preservando os fluxos funcionais e as regras de negócio essenciais definidos no documento de Visão e Escopo.

Em atendimento à tarefa da squad, o documento concentra-se em quatro entregas: contexto do projeto, requisitos funcionais, casos de uso (diagrama e descrição) e rastreabilidade entre requisitos funcionais e casos de uso.

### 1.2 Escopo

A SRS aplica-se ao ciclo operacional de eventos acadêmicos: cadastro e reserva de auditórios, criação e gestão de eventos, inscrição de participantes, fila de espera, controle de presença e emissão de certificados. A forma de implementação e as plataformas de disponibilização permanecem em aberto, desde que os requisitos e as regras aqui especificados sejam preservados.

### 1.3 Definições, acrônimos e abreviações

| Termo | Definição |
|---|---|
| SRS | Software Requirements Specification — Especificação de Requisitos de Software. |
| RF | Requisito Funcional. |
| UC | Use Case — Caso de Uso. |
| RN | Regra de Negócio. |
| Administrador / Organizador | Perfil responsável por cadastrar locais, criar eventos, realizar check-in e acompanhar a operação. |
| Participante | Perfil que consulta eventos, inscreve-se, realiza check-in e obtém certificados. |
| Auditório / Local | Espaço físico cadastrado para realização de eventos, com capacidade e localização. |
| Subevento | Palestra, sessão ou atividade vinculada a um evento principal. |
| Fila de espera | Lista ordenada de participantes aguardando vaga quando o evento está lotado. |
| Check-in | Registro auditável de presença no evento, preferencialmente por chip do crachá ou QR Code. |
| Certificado | Comprovante de participação emitido somente a quem teve presença registrada, com código único de verificação. |

### 1.4 Referências

- Visão e Escopo do Projeto — Sistema de Gestão de Eventos e Auditórios (documento-base para desenvolvimento).
- MackLEAPS template — Software Requirements Specification (RUP).
- IEEE Std 830-1998 — Recommended Practice for Software Requirements Specifications.
- UML 2.x — Diagrama de Casos de Uso.

### 1.5 Visão geral do documento

A Seção 2 descreve o contexto do projeto. A Seção 3 especifica os requisitos funcionais. A Seção 4 apresenta o diagrama e a descrição dos casos de uso. A Seção 5 registra a rastreabilidade, indicando quais requisitos funcionais originaram quais casos de uso.

---
