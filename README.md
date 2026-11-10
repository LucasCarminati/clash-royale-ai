# Clash Royale AI Agent

Projeto experimental de Inteligência Artificial voltado ao estudo de estratégias, tomada de decisão e simulação de partidas inspiradas em Clash Royale.

O objetivo é desenvolver progressivamente um agente capaz de representar o estado de uma partida, analisar possíveis decisões e selecionar ações utilizando diferentes técnicas de Inteligência Artificial.

## Roadmap

O projeto será desenvolvido de forma incremental, em cinco fases:

### Fase 1 — Fundação

- representação do estado da partida (`GameState`);
- sistema de cartas, com atributos em arquivos de dados;
- gerenciamento de elixir;
- rastreamento do ciclo de cartas.

### Fase 2 — Simulador

- loop de simulação em ticks, determinístico;
- representação da arena;
- motor básico de combate;
- separação entre estado, observação e ação;
- interface de ambiente no padrão Gymnasium (`reset` / `step`).

### Fase 3 — Agentes clássicos

- agente aleatório e agente baseado em regras;
- avaliação por taxa de vitória em múltiplas partidas;
- busca com Monte Carlo Tree Search adaptado.

### Fase 4 — Aprendizado

- aprendizado por imitação;
- Reinforcement Learning com self-play.

### Fase 5 — Mundo real

- visão computacional (detecção de objetos e OCR);
- análise de replays;
- testes contra a IA nativa do jogo.

## Arquitetura

```text
Simulador (GameState)
    │  observação: o que o agente consegue ver
    ▼
Agente
    │  ação: jogar uma carta em uma posição, ou esperar
    ▼
Simulador avança um tick
    │
    └──► repete até o fim da partida
```

O `GameState` é o estado completo e verdadeiro da partida dentro do simulador. O agente não recebe o `GameState` inteiro, apenas uma observação: ele não vê, por exemplo, as cartas na mão do adversário.

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
- pytest (testes automatizados)
- Gymnasium (interface padrão de ambientes de simulação)

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

Estrutura planejada. Até o momento, apenas `src/models/` e `docs/` existem no repositório; as demais pastas serão criadas conforme cada fase for iniciada.

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

O desenvolvimento e o treinamento acontecem em um simulador próprio. O projeto não tem como objetivo automatizar partidas contra outros jogadores, o que violaria os termos de serviço do jogo. Eventuais testes no jogo real ficam restritos a partidas contra a IA nativa.

Clash Royale e suas marcas relacionadas pertencem à Supercell. Este projeto não possui associação, patrocínio ou afiliação com a Supercell.
