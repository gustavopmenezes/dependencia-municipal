# Hipóteses e testes, escritos antes de rodar

Registrado em 05/10/2026, antes de qualquer teste estatístico. O que já tinha sido visto nesse momento: as
medianas descritivas de São Paulo e do Maranhão em 2024, por faixa de população. Os outros onze estados do
Nordeste e do Sudeste ainda não tinham sido olhados, e nenhum ano além de 2024. Por isso os testes de SP
contra MA são leitura exploratória (a hipótese foi ajustada vendo o dado), e os de Sudeste contra Nordeste e
os de evolução no tempo são confirmatórios.

## Regras que valem para todos

- Unidade: município com contas anuais (DCA) utilizáveis no ano. Não é amostra, é o universo. O valor-p
  responde a "essa diferença caberia no acaso de um processo que gera municípios parecidos?", e pesa menos
  que o tamanho do efeito. Todo teste sai com tamanho de efeito e intervalo de 95%.
- Comparação de dois grupos: Mann-Whitney bilateral, diferença de medianas de Hodges-Lehmann com intervalo
  por reamostragem (2.000 repetições, semente fixa) e delta de Cliff.
- "Em município do mesmo tamanho": regressão por mínimos quadrados com log da população e indicadora do
  grupo, erro-padrão robusto HC3, nos municípios de até 50 mil habitantes. O coeficiente da indicadora é a
  diferença a tamanho igual. Repete-se por faixa (5 a 10 mil, 10 a 20 mil, 20 a 50 mil) com Mann-Whitney.
- Proporções: teste exato de Fisher e intervalo de Wilson.
- Evolução: diferença dentro do mesmo município entre dois anos, teste de postos com sinal de Wilcoxon.
- Correção de Holm dentro de cada família (A a G). Nível de 5% depois da correção.
- População das faixas: Censo 2022. Valores por habitante: estimativa do IBGE do ano.
- Receita: a base definida em `docs/METODO.md` (líquida das deduções, sem previdência própria, sem
  empréstimo e sem venda de bens). Toda conclusão é refeita na especificação alternativa (FPM e ICMS brutos,
  FUNDEB pelo saldo); se mudar de sinal, a conclusão cai para "depende da contabilidade".

## Família A: dependência em parcela da receita

- A1. Nos municípios de até 50 mil habitantes, a parcela da receita que vem de transferências é diferente
  entre SP e MA a tamanho igual. Expectativa: MA mais alto, entre 5 e 15 pontos.
- A2. O mesmo para a autonomia (tributos próprios sobre a receita). Expectativa: SP mais alto.
- A3. O mesmo para a autonomia sem o imposto de renda retido na fonte.
- A4. Sudeste contra Nordeste, mesmas três medidas.

## Família B: dependência por habitante

- B1. A tamanho igual, as transferências por habitante são diferentes entre SP e MA. Expectativa do dono:
  SP recebe mais. O que as medianas sugerem: diferença pequena, MA um pouco acima de 5 mil habitantes.
- B2. Sudeste contra Nordeste, a tamanho igual.
- B3. Entre os municípios de até 5 mil habitantes do Sudeste, as transferências por habitante superam as dos
  municípios de 10 a 20 mil habitantes do Nordeste (o município nordestino típico). Expectativa: sim.

## Família C: a maior fatia

- C1. A proporção de municípios em que o FPM é a maior fatia é maior em SP que no MA.
- C2. A proporção em que o FUNDEB é a maior fatia é maior no MA que em SP.
- C3. As duas, Sudeste contra Nordeste.

## Família D: dinheiro que depende de convênio, pleito ou emenda

- D1. A parcela de transferências voluntárias registradas na DCA (convênios, transferências especiais e
  transferências de capital) é maior em SP que no MA a tamanho igual.
- D2. Sudeste contra Nordeste.
- D3. As emendas federais pagas a prefeituras e fundos municipais em 2025, por habitante (Portal da
  Transparência), são maiores no MA que em SP a tamanho igual. Expectativa: MA mais alto, pela regra de
  cotas por parlamentar e por bancada.
- Ressalva escrita antes: D1 e D2 medem o que cada prefeitura classificou como convênio. A pesquisa mostrou
  que a conta própria da emenda Pix registra 68% do valor pago em SP e 15% numa amostra do MA. Um resultado
  a favor de SP em D1 pode ser em parte efeito de classificação.

## Família E: custo da máquina

- E1. O gasto por habitante com Câmara e administração (funções 01 e 04) cai com a população: elasticidade
  negativa na regressão log-log com efeito fixo de estado. Expectativa: entre -0,2 e -0,5.
- E2. A tamanho igual, esse gasto por habitante é diferente entre SP e MA, e entre Sudeste e Nordeste.
- E3. A proporção de municípios em que os tributos próprios não cobrem esse gasto é maior no MA que em SP,
  e no Nordeste que no Sudeste.

## Família F: limiares do FPM

- F1. Há mais municípios logo acima do que logo abaixo dos limiares de faixa do FPM do que uma densidade
  suave produziria (janela de 2% de cada lado, 17 limiares somados, teste binomial). Com a população do
  Censo 2022 a expectativa é não haver excesso; com as estimativas anteriores ao Censo, sim. Só a primeira
  parte é testável agora.

## Família G: evolução no tempo

- G1. Entre o primeiro e o último ano disponível, a dependência de transferências dos municípios de até
  20 mil habitantes mudou (por estado e por região).
- G2. O mesmo para a parcela do FPM e para a parcela do FUNDEB.
- G3. O mesmo para o gasto por habitante com a máquina, em valores corrigidos pelo IPCA.
- Com a série longa (2013 em diante): tendência linear com efeito fixo de município e erro agrupado por
  município, e Mann-Kendall sobre as medianas anuais.

## Desvios do registro

- 05/10/2026, antes de rodar: onde os dois grupos somam mais de 300 mil pares (comparações entre regiões), o
  intervalo da diferença de Hodges-Lehmann é o de Moses, que sai da ordem das diferenças, e não o de
  reamostragem. O motivo é só tempo de máquina; os dois são intervalos de 95% para a mesma quantidade.

- 05/10/2026, antes de rodar: as transferências de instituições privadas, de pessoas e do exterior saíram do
  grupo de transferências (não são dinheiro de outro governo).
- 05/10/2026, depois da primeira rodada de testes e da conferência independente (`revisao/claude/`). Tudo o que
  segue foi decidido vendo resultado, e por isso as linhas novas de `docs/TESTES.md` levam a marca
  "pós-verificação":
  - a base ganhou crivos de plausibilidade e perdeu 106 municípios (94 por dedução do FUNDEB incoerente);
  - as transferências de capital de instituições privadas saíram da receita-base;
  - B1 foi partido em "até 5 mil" e "5 a 50 mil habitantes", porque o efeito muda com o tamanho;
  - E1 ganhou elasticidade por trecho e E2 ganhou a versão na mediana (regressão quantílica);
  - D1 foi partido em verba da União e verba do estado;
  - nas comparações entre regiões o p passou a ser o maior entre o robusto e o agrupado por estado; com isso
    B1 entre Sudeste e Nordeste deixou de ser distinguível de zero;
  - o intervalo da diferença de proporções passou a ser o de Newcombe;
  - a família G foi rodada sobre a série longa do IPEADATA, começando em 2002 e não no primeiro ano
    disponível, porque 2000 e 2001 têm outra classificação.
- Expectativa errada, registrada: em F1 eu esperava não haver excesso de municípios acima dos degraus do FPM no
  Censo 2022. Há.
- Ainda não foi feito do que estava registrado: refazer B, D e E na especificação alternativa, e o teste de
  Mann-Kendall da família G.
- 06/10/2026, depois da revisão cruzada do GPT e do Grok (`revisao/claude/CONCILIACAO-RODADA-1.md` e
  `APLICADO-RODADA-1.md`). Tudo decidido vendo resultado:
  - D1 mudou de medida. O registro dizia "convênios, transferências especiais e transferências de capital". A
    medida principal passou a ser a restrita, sem o SUS de convênio e de capital e sem o convênio corrente
    estadual de educação (`pct_voluntarias_restrita` e as duas por pagador). A medida do registro continua em
    `docs/TESTES.md` com os ids D1am, D1uam e D1eam, como sensibilidade. As linhas da restrita levam a marca
    "pós-verificação". Com mais linhas na família D, a correção de Holm ficou mais dura: a diferença de verba
    federal entre Sudeste e Nordeste deixou de ser distinguível de zero (p de 0,016 para 0,066);
  - a receita-base mudou: ICMS e IPI lançados como imposto próprio viraram cota (18
    municípios), e a assistência à saúde dos servidores (1.6.3.2.01) e as contribuições previdenciárias
    1.2.1.9.50 saíram da base (14 municípios). A1 entre São Paulo e Maranhão não mudou (13,5 pontos); entre as
    regiões foi de 6,698 para 6,704 pontos. Salto/SP mudou de maior fatia;
  - o motivo de exclusão "dedução do FUNDEB" foi partido em dois (93 fora da faixa, 1 sem cesta); ninguém entrou
    nem saiu: seguem 3.356 municípios;
  - família S, nova: A1 e C1 sem os 100 municípios com alerta de FPM ou de FUNDEB. Não muda a leitura;
  - família R, nova: o oeste paulista contra o resto do estado a tamanho igual (pedido do Grok para a seção
    12). Não se distingue de zero;
  - B1 (único até 50 mil habitantes, -9,3%) voltou a ser o número de referência de 4.1, ao lado de B1x
    (-11,6%), que é pós-verificação;
  - triênio 2023 a 2025 para São Paulo e Maranhão (ideia e primeira conta do GPT, refeita em
    `revisao/claude/apoio/r1_numeros_extras.py`): não estava no registro; serve de faixa;
  - seção 13, classe única de dependência por corte: descritiva, sem teste.
- Ainda não foi feito do que a conciliação listou: teste de densidade nos degraus dentro do pipeline (o pacote
  `rddensity` não está no ambiente; vale o do GPT), regras por plano de contas antes de 2022 e a harmonização
  dos depósitos não identificados (1.7.9.2).

## O que derruba a tese do dono, dito antes

A tese: "o interior profundo de SP depende de verba externa e de deputado tanto quanto, ou mais que, o
Maranhão". Ela se divide em três, e cada parte cai sozinha:

1. Em parcela da receita: cai se A1 der MA acima de SP em todas as faixas com intervalo que não cruza zero.
2. Em reais por habitante: cai se B1 der MA acima de SP; fica de pé em versão mais fraca se só B3 passar
   (o efeito é de composição: SP tem muito município minúsculo, o MA quase nenhum).
3. Em verba de deputado: cai se D3 der MA acima de SP e D1 não resistir à ressalva de classificação.
