# Nota de método: quem fez o quê

Este estudo foi feito por uma pessoa e por modelos de linguagem de quatro empresas, entre 5 e 6 de outubro de 2026. A divisão do
trabalho faz parte do método e por isso fica escrita.

## O que o autor fez

Gustavo Menezes fez as perguntas, e são elas que dão a forma do estudo:

- a pergunta de partida: o interior profundo de São Paulo (o oeste do estado e o Vale do Ribeira) dependeria de
  receita externa em maior proporção que o Maranhão? E o palpite de que cerca de 80% dos municípios paulistas têm menos de 50 mil habitantes (são 78,8%);
- a ideia de pintar cada município pela maior fatia da receita, e de estender a comparação a todo o Nordeste e o
  Sudeste;
- o pedido de ver a evolução no tempo com dispersão, municípios fora da curva contados e teste estatístico das
  afirmações;
- as perguntas da segunda rodada: se dependência pode ser uma classe só, se a teoria de escala urbana explica o
  que se vê, o que a representação no Congresso tem com isso, e a linha do tempo das emendas;
- as fontes de fora: a nota técnica do Centro de Estudos da Metrópole, da qual discorda, e os vídeos do debate
  público, com o pedido de ler todos com a mesma desconfiança;
- as perguntas da terceira rodada: se a proporção entre as fontes de receita difere muito entre as regiões, o que
  é cada fonte e que mecanismo a garante, quanto do território os municípios pequenos administram, e de quem era
  o projeto de 2019 que a imprensa chamou de extinção de municípios;
- as perguntas da quarta rodada: se o gráfico da capa melhoraria mais largo, com um histograma atrás do outro,
  em quantidade ou em % dos municípios, e no acumulado; como usar o termo "regiões" sem confundir (Grandes
  Regiões e regiões geográficas intermediárias do IBGE); e o pedido de trocar a suspeita de partida por uma
  pergunta de partida, imparcial, com um balão de confundidores: como a pergunta redigida pode ir para direções
  diferentes conforme a leitura das palavras, e o que precisou ser assumido.

Também decidiu a forma (mapa estático com geopandas, preto e branco onde há uma variável só, cor onde há
comparação), o vocabulário (receita externa e receita interna; "interior profundo" para o oeste paulista e o
Vale do Ribeira) e montou a conferência cruzada: levou os pedidos ao GPT, ao Grok, ao Gemini e ao ChatGPT e
trouxe as respostas de volta.

## O que os modelos fizeram

| Modelo | Papel | O que entregou |
|---|---|---|
| Claude (Anthropic) | executor e conciliador | download e classificação das contas, base por município, figuras, testes, pesquisa das regras e da literatura por agentes, conferência interna, conferência do que os outros modelos trouxeram, deck e e-book em PDF |
| GPT, no Codex (OpenAI) | auditor e replicador | réplica cega da receita de 150 municípios, auditoria da classificação contra o ementário oficial, triênio de 2023 a 2025, teste de densidade nos degraus do FPM, proposta para os planos de contas antigos; na rodada 2, réplica independente da base inteira e 33 correções |
| Grok (xAI) | contraditor e checagem na web | o melhor argumento contra cada achado, conferência de fatos e datas, o que mudou em 2025 e 2026; na rodada 2, leitura do site como leitor hostil e como leitor leigo, e as vozes que faltavam no debate |
| Gemini (Google), pesquisa profunda | busca de literatura e de bases | pistas de leitura e de dados; entrou só o que foi aberto na fonte |
| ChatGPT (OpenAI), pesquisa profunda | busca de literatura e de contradições | pistas de leitura; entrou só o que foi aberto na fonte |

## O tamanho do trabalho

- 31.149 declarações de contas anuais de 2017 a 2025 baixadas da API do Tesouro, uma por município e ano (cerca de
  uma chamada por segundo; as de 2013 a 2016 ainda estavam sendo baixadas e não entram no estudo), 50 séries
  municipais do IPEADATA, o arquivo de emendas do Portal da Transparência, malhas e censos do IBGE, CAPAG e IFGF:
  2,0 GB de dado bruto. Contagem de `dados/bruto/siconfi/dca` e tamanho de `dados/bruto` em 06/10/2026.
- Cerca de 3 mil linhas de código do estudo e mais de uma centena de scripts de apoio e de conferência.
- Mais de 130 testes estatísticos, com as hipóteses escritas antes de rodar; 69 figuras (arquivos em `figuras/`
  em 06/10/2026, com as do painel das regiões); 13 frentes de pesquisa documental na primeira montagem e mais
  quatro na rodada 2; 74 fontes baixadas e fichadas na primeira montagem (`fontes/INDICE.md`); 171 referências
  conferidas (`docs/REFERENCIAS.md`).
- Oito agentes de conferência interna, duas auditorias do GPT, duas revisões do Grok e duas pesquisas profundas.
- Um deck interativo em Slidev e um e-book em PDF, escritos, montados e conferidos por captura de tela por
  agentes, com um revisor para casar citação e referência.

Estimativa, grosseira e por baixo: uma pessoa com prática em finanças públicas e programação levaria de quatro a
oito semanas para chegar ao mesmo ponto. Aqui foram menos de dois dias de relógio. O que encolheu foi a execução.
O que não encolheu: decidir o que perguntar e saber quando desconfiar.

## O que a conferência derrubou

A primeira versão dos achados tinha erros que só apareceram quando outro agente refez a conta por outro caminho.
A conferência interna derrubou onze frases (lista no fim de `docs/ACHADOS.md`). A revisão do GPT e do Grok mudou a
medida de verba negociada, que incluía o SUS, e a leitura de três seções. Nenhuma das rodadas achou erro de
aritmética na base: os erros estavam na leitura e na classificação.

## Rodada 2

Em 06/10/2026, com o deck e o relatório já publicados em versão anterior, chegaram quatro devolutivas e uma lista
de pedidos do autor. A conciliação está em `revisao/claude/CONCILIACAO-RODADA-2.md`.

| Quem | O que fez | O que mudou |
|---|---|---|
| GPT, no Codex | Refez a base de 2024 das folhas brutas, sem importar o código do projeto, e auditou o relatório e o deck | Confirmou as conclusões centrais. Achou dois defeitos de classificação: convênios de capital da saúde dentro da medida "sem SUS" (R$ 435 milhões) e capital privado contado como receita corrente (R$ 3,3 bilhões, em colunas que nenhum achado usava). Achou a contagem por corte do deck feita depois de arredondar, um rótulo errado na série de emendas e dez arredondamentos de último algarismo |
| Grok | Leu o site como leitor hostil e como leitor leigo, conferiu datas e procurou vozes ausentes | O tom: carimbos de veredito sobre conta exploratória, "não bate" onde a fonte definia o indicador, percentuais tirados de 62 comentários, um número grande que viajava como resultado. Trouxe o prefeito de município pequeno, o parlamentar que defende emenda e gente do Nordeste |
| Gemini e ChatGPT, pesquisa profunda | Buscaram literatura, bases de dados e contradições | Pistas. Depois da conferência ficaram a nota do IPEA sobre a reforma tributária, a lei paulista de emancipações, as referências certas dos estudos de fusão e dos degraus do FPM, e seis números das fichas que estavam "de memória" e passaram a conferidos. Nenhuma das contradições apontadas derrubou achado |
| Claude | Refez cada correção do GPT, abriu cada fonte das pesquisas profundas, conferiu os fatos pedidos pelo autor, refez a base com as duas correções e com 2022 a 2025 dos 13 estados | A verba estadual a tamanho igual foi de 2,3 para 2,2 pontos e a verba negociada sobre o investimento, de 53% para 49%. O triênio dos 13 estados respondeu que o ano de eleição não distorce o retrato entre as regiões. Entraram a pizza média por região, a parcela do território por tamanho de município e o glossário das oito fontes de receita |
| O autor | Pediu a questão-chave no começo, o vocabulário, as explicações de cada fonte e o contexto do projeto de 2019 | O deck mudou de desenho em vários slides; a posição do autor passou a aparecer só sob esse rótulo |

## Avisos

Erros confiantes dos próprios modelos, e um do autor, que ficam como aviso:

- Uma análise de vídeo trazida para o estudo não conferia com o vídeo: título errado, números e comentários que
  não existiam.
- Várias datas e números de literatura vieram "de memória" e estão marcados assim nos arquivos de pesquisa até
  alguém abrir a fonte.
- **Pesquisa profunda de modelo inventa referência com cara de certa.** Três exemplos desta rodada, todos com
  autor, revista e página. (1) Caselli e Michaels (2013) apareceu como estudo de fusão de municípios em
  Pernambuco, com 9% de economia e a marca "lido"; o artigo é sobre royalties de petróleo e não trata de fusão.
  (2) "Blom-Hansen, Houlberg e Serritzlew (2014), American Political Science Review, 108(4), p. 791-807" não
  existe: mistura um artigo de 2014 de outra revista com um de 2016 (o certo é v. 110, n. 4, p. 812-831). (3) O
  multiplicador local do FPM em Corbi, Papaioannou e Surico (2019) veio como 0,6 a 0,8; o artigo diz perto de 2.
  A marca "lido" do modelo não vale como conferência, e o "não encontrei" dele não quer dizer que a obra não
  existe: um artigo sobre municípios brasileiros foi dado como inexistente. As listas completas estão no fim de
  `docs/pesquisa/pesquisa-profunda-gemini.md` e de `pesquisa-profunda-chatgpt.md`.
- **A lembrança do autor também foi conferida, e uma não se sustentou.** O autor lembrava o vídeo de 2019 sobre
  as cidades que sairiam do mapa como peça de um contexto anti-bolsonarista. As fontes descrevem o jornal que o
  publicou, naquele período, como de linha editorial à direita e favorável às reformas do Ministério da Economia.
  O que se sustenta é outra coisa: o texto da proposta dizia "incorporado", e os títulos da imprensa, inclusive o
  da agência oficial, disseram "extinguir". Também não foi localizado registro de motivação eleitoral ou
  regional para a proposta, nem fala do ministro com a palavra "fusão". O deck diz o que as fontes dizem do
  jornal, registra o que não foi achado e traz a leitura do autor sobre o verbo só sob o rótulo "posição do
  autor" (`docs/pesquisa/fatos-rodada-3.md`, 2e e 2f).

## O que isso permite afirmar

- Os números vêm de dado público e de código que qualquer pessoa pode rodar de novo; o método está em
  `docs/METODO.md`.
- Conferência entre modelos não é revisão por pares. Modelos que leram os mesmos textos podem errar juntos.
- O estudo descreve; não prova causa. Onde arrisca um mecanismo (a escada do FPM, o custo fixo da prefeitura), diz
  com que conta.
- As conclusões de política ficam com o leitor. O deck mostra as opções e o que a evidência diz de cada uma.
