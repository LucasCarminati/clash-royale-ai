# Clash Royale AI Agent

Projeto experimental de Inteligência Artificial voltado ao estudo de estratégias, tomada de decisão e simulação de partidas inspiradas em Clash Royale.

O objetivo é desenvolver progressivamente um agente capaz de representar o estado de uma partida, analisar possíveis decisões e selecionar ações utilizando diferentes técnicas de Inteligência Artificial.

## Objetivos

O projeto será desenvolvido de forma incremental, passando por diferentes níveis de complexidade:

- representação completa do estado da partida;
- sistema de cartas;
- gerenciamento de elixir;
- rastreamento de ciclo de cartas;
- representação da arena;
- motor de combate;
- agentes baseados em regras;
- avaliação e pontuação de jogadas;
- simulação de partidas;
- Monte Carlo Tree Search (MCTS);
- Machine Learning;
- Reinforcement Learning;
- visão computacional para análise de partidas.

## Arquitetura inicial

```text
Game State
    │
    ▼
Decision Engine
    │
    ▼
Possible Actions
    │
    ▼
Evaluation / Simulation
    │
    ▼
Best Action
```

## Tecnologias

Inicialmente:

- Python
- Git
- GitHub

Tecnologias previstas para etapas posteriores:

- OpenCV
- PyTorch
- Machine Learning
- Reinforcement Learning
- Monte Carlo Tree Search

## Estrutura

```text
src/
├── models/
├── engine/
├── agents/
├── simulation/
└── vision/

tests/
docs/
```

## Estado atual

### Etapa 1 — Representação do estado da partida

Em desenvolvimento.

A primeira etapa consiste na criação do `GameState`, estrutura responsável por representar todas as informações relevantes de uma partida em determinado instante.

Entre as informações planejadas estão:

- tempo restante;
- elixir do jogador;
- estimativa de elixir do adversário;
- cartas disponíveis;
- próxima carta;
- estado das torres;
- tropas presentes na arena;
- posições das unidades.

## Documentação

A documentação técnica completa e o histórico de desenvolvimento estão disponíveis em:

```text
docs/PROJECT_DOCUMENTATION.md
```

## Aviso

Este projeto possui finalidade educacional e experimental, com foco em Engenharia de Software, Inteligência Artificial, algoritmos e simulação.

Clash Royale e suas marcas relacionadas pertencem à Supercell. Este projeto não possui associação, patrocínio ou afiliação com a Supercell.