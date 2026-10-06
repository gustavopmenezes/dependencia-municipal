# Nota de método: quem fez o quê

Este estudo foi feito por uma pessoa e três modelos de linguagem, entre 5 e 6 de outubro de 2026. A divisão do
trabalho faz parte do método e por isso fica escrita.

## O que o autor fez

Gustavo Paixão Menezes fez as perguntas, e são elas que dão a forma do estudo:

- a tese de partida: o interior de São Paulo depende de verba de fora e de deputado tanto quanto o Maranhão, e o
  palpite de que cerca de 80% dos municípios paulistas têm menos de 50 mil habitantes (são 78,8%);
- a ideia de pintar cada município pela maior fatia da receita, e de estender a comparação a todo o Nordeste e o
  Sudeste;
- o pedido de ver a evolução no tempo com dispersão, municípios fora da curva contados e teste estatístico das
  afirmações;
- as perguntas da segunda rodada: se dependência pode ser uma classe só, se a teoria de escala urbana explica o
  que se vê, o que a representação no Congresso tem com isso, e a linha do tempo das emendas;
- as fontes de fora: a nota técnica do Centro de Estudos da Metrópole, da qual discorda, e os vídeos do debate
  público, com o pedido de ler todos com a mesma desconfiança.

Também decidiu a forma (mapa estático com geopandas, preto e branco onde há uma variável só, cor onde há
comparação) e montou a conferência cruzada: levou os pedidos ao GPT e ao Grok e trouxe as respostas de volta.

## O que os modelos fizeram

| Modelo | Papel | O que entregou |
|---|---|---|
| Claude (Anthropic) | executor e conciliador | download e classificação das contas, base por município, figuras, testes, pesquisa das regras e da literatura por agentes, conferência interna, deck e PDF |
| GPT, no Codex (OpenAI) | auditor e replicador | réplica cega da receita de 150 municípios, auditoria da classificação contra o ementário oficial, triênio de 2023 a 2025, teste de densidade nos degraus do FPM, proposta para os planos de contas antigos |
| Grok (xAI) | contraditor e checagem na web | o melhor argumento contra cada achado, conferência de fatos e datas, o que mudou em 2025 e 2026 |

## O tamanho do trabalho

- 15,6 mil declarações de contas anuais baixadas da API do Tesouro (uma por município e ano, cerca de uma por
  segundo), 50 séries municipais do IPEADATA, o arquivo de emendas do Portal da Transparência, malhas e censos do
  IBGE, CAPAG e IFGF: 1,6 GB de dado bruto.
- Cerca de 3 mil linhas de código do estudo e uma centena de scripts de apoio e de conferência.
- Mais de 130 testes estatísticos, com as hipóteses escritas antes de rodar; 62 figuras; 13 frentes de pesquisa
  documental; 74 fontes baixadas e fichadas (`fontes/INDICE.md`).
- Oito agentes de conferência interna, uma revisão do GPT e uma do Grok.
- Um deck interativo de 53 slides e um relatório em PDF, escritos, montados e conferidos por captura de tela por
  agentes, com um revisor para casar citação e referência.

Estimativa, grosseira e por baixo: uma pessoa com prática em finanças públicas e programação levaria de quatro a
oito semanas para chegar ao mesmo ponto. Aqui foi menos de um dia de relógio. O que encolheu foi a execução.
O que não encolheu: decidir o que perguntar e saber quando desconfiar.

## O que a conferência derrubou

A primeira versão dos achados tinha erros que só apareceram quando outro agente refez a conta por outro caminho.
A conferência interna derrubou onze frases (lista no fim de `docs/ACHADOS.md`). A revisão do GPT e do Grok mudou a
medida de verba negociada, que incluía o SUS, e a leitura de três seções. Nenhuma das duas rodadas achou erro de
aritmética na base: os erros estavam na leitura.

Dois exemplos de erro confiante dos próprios modelos, que ficam como aviso: uma análise de vídeo trazida para o
estudo não conferia com o vídeo (título errado, números e comentários que não existiam), e várias datas e números
de literatura vieram "de memória" e estão marcados assim nos arquivos de pesquisa até alguém abrir a fonte.

## O que isso permite afirmar

- Os números vêm de dado público e de código que qualquer pessoa pode rodar de novo; o método está em
  `docs/METODO.md`.
- Conferência entre modelos não é revisão por pares. Três modelos que leram os mesmos textos podem errar juntos.
- O estudo descreve; não prova causa. Onde arrisca um mecanismo (a escada do FPM, o custo fixo da prefeitura), diz
  com que conta.
- As conclusões de política ficam com o leitor. O deck mostra as opções e o que a evidência diz de cada uma.
