# Diagrama de Sequência

O diagrama de sequência representa a interação entre o participante e os componentes do sistema durante o processo de inscrição em um evento.

## Inscrição em Evento

O fluxo está relacionado principalmente aos casos de uso:

- UC06 — Inscrever-se em evento
- UC08 — Ingressar na fila de espera

### Fluxo principal

1. O participante solicita a inscrição.
2. O sistema verifica se já existe inscrição.
3. O sistema verifica a disponibilidade de vagas.
4. Se houver vaga, a inscrição é confirmada.
5. Se não houver vaga e a fila estiver habilitada, o participante é incluído na fila de espera.

## Diagrama

<img width="1472" height="2230" alt="image" src="https://github.com/user-attachments/assets/6544b489-8dd5-4d70-9aed-8d8243f86cdf" />
