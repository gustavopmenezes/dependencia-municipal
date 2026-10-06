# Achados

Retrato das contas de 2024 dos municípios do Nordeste e do Sudeste (3.356 com contas utilizáveis, de 3.462) e
evolução de 2002 a 2025. Todo número daqui sai de `docs/NUMEROS.md`, `docs/TESTES.md`, `docs/tabelas/` ou de
`revisao/claude/apoio/r1_numeros_extras.txt` e, na seção 15, de `revisao/claude/r3/PIPELINE-RODADA-3.md` e de
`docs/pesquisa/fatos-rodada-3.md`. O método está em `docs/METODO.md`. Versão de 06/10/2026, corrigida
pela conferência interna (`revisao/claude/`), pela revisão cruzada do GPT e do Grok
(`revisao/claude/CONCILIACAO-RODADA-1.md`) e pela segunda rodada de revisão, com duas pesquisas profundas
(`revisao/claude/CONCILIACAO-RODADA-2.md` e `revisao/claude/r3/PIPELINE-RODADA-3.md`). O que cada uma mudou
está na seção 15 e no fim.

Vocabulário. **Receita** é o total que entra na prefeitura. **Receita externa**, ou de fora do município, é o
que a União e o estado repassam: FPM, FUNDEB, cota do ICMS e do IPVA, SUS, royalties e outras transferências.
**Receita interna**, ou própria, é o que o município arrecada: tributos próprios e demais receitas próprias.
**Dependência** é a soma das seis fontes externas sobre a receita. Parte da receita externa tem destino
obrigatório (o FUNDEB vai para a escola, o SUS para a saúde). **Verba negociada** é convênio, transferência de
capital e emenda, na medida restrita, sem o SUS. **Interior profundo** é como o autor chama o oeste paulista e
o Vale do Ribeira.

## Resposta curta

A tese "o interior profundo de São Paulo depende de verba externa e de deputado tanto quanto, ou mais que, o
Maranhão" tem uma parte que vale em número de prefeituras, uma que empata e duas que caem.

- **Vale em número de prefeituras, e depende do corte.** São Paulo tem 150 municípios de até 5 mil habitantes;
  o Maranhão tem 5. Nos paulistas, 90% da receita é externa e cada morador recebe em torno de R$ 9,2 mil por
  ano de fora do município, 72% a mais que no município maranhense típico (R$ 5,4 mil). Acima de 80% de
  dependência há mais prefeituras em São Paulo: 338 (53,8% das paulistas) contra 210 no Maranhão (97,7% das
  maranhenses). Acima de 90%, o Maranhão tem o dobro: 184 (85,6%) contra 92 em São Paulo (14,6%). Em proporção
  dos municípios, o Maranhão fica acima em todo corte de 50% a 95% (seção 13). O FPM é a maior fonte em 53% dos
  municípios paulistas e em 7% dos maranhenses; com o FUNDEB contado pelo saldo, em 55% e 35%.
- **Empata em reais por habitante no município minúsculo, entre as regiões.** Até 5 mil habitantes, Sudeste e
  Nordeste recebem o mesmo por habitante (R$ 8,9 mil e R$ 8,5 mil; diferença indistinguível de zero). Para São
  Paulo contra o Maranhão nessa faixa não dá para dizer: são cinco municípios maranhenses. De 5 a 50 mil
  habitantes, o paulista recebe de 9% a 12% a menos que o maranhense do mesmo tamanho, conforme o recorte e os
  anos.
- **Cai em parcela da receita.** Em toda faixa de população o município maranhense depende mais: 13,5 pontos
  percentuais a mais até 50 mil habitantes. O Nordeste, 6,7 pontos a mais que o Sudeste.
- **Cai na verba de deputado federal.** As emendas federais pagas em 2025 dão R$ 149 por habitante na mediana
  dos municípios paulistas de até 20 mil habitantes, a menor entre os 13 estados; no Maranhão, R$ 357; em
  Sergipe, R$ 670. O que São Paulo tem a mais é convênio com o governo do estado: 2,5% da receita, contra 0,0%
  na mediana maranhense.

O que é pouco intuitivo não é São Paulo parecer com o Maranhão. É que **Minas Gerais, o Rio Grande do Norte, a
Paraíba e o Piauí** é que parecem com o interior paulista (muito município minúsculo vivendo de FPM), e que o
Maranhão é um caso à parte dentro do próprio Nordeste (quase tudo vem do FUNDEB e quase não há município
minúsculo). Essa semelhança depende da contabilidade: com o FUNDEB pelo saldo, o FPM lidera em mais municípios
do Nordeste que do Sudeste (2.3).

Na pizza do município médio as duas regiões se parecem mais do que a tese e a antítese supõem: a receita
externa é 83% no Sudeste e 91% no Nordeste, e o FPM pesa o mesmo, 30% e 30%. A diferença está em qual fonte
externa completa a conta (15.5).

## 1. Quantos municípios são pequenos

| | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| Municípios | 645 | 217 | 1.668 | 1.794 |
| Até 50 mil habitantes | 508 (78,8%) | 195 (89,9%) | 1.411 (84,6%) | 1.619 (90,2%) |
| População que mora neles | 15,1% | 51,7% | 20,8% | 44,5% |
| Até 10.188 hab. (menor faixa do FPM) | 275 (42,6%) | 44 (20,3%) | 776 (46,5%) | 630 (35,1%) |
| Até 5 mil habitantes | 150 (23,3%) | 5 (2,3%) | 397 (23,8%) | 248 (13,8%) |

Contagens e percentuais de população usam os 3.462 municípios. Percentuais de receita usam os 3.356 com
contas utilizáveis.

1.1. O palpite dos 80% estava certo: 78,8% dos municípios paulistas têm até 50 mil habitantes. Neles mora
15,1% da população do estado, entra 14,9% da receita municipal e só 5,5% dos tributos próprios.

1.2. A diferença entre os dois estados está na ponta de baixo. Quatro em cada dez municípios paulistas estão na
menor faixa do FPM; no Maranhão, dois em cada dez. Como o Maranhão só tem cinco municípios de até 5 mil
habitantes, toda comparação nessa faixa entre os dois estados é frágil; a que vale é Sudeste contra Nordeste.

1.3. Esta seção descreve a malha de municípios, não a dependência. Contar prefeituras dependentes exige
escolher um corte, e a resposta muda com ele: acima de 80% de dependência, 338 em São Paulo e 210 no Maranhão;
acima de 90%, 92 e 184 (seção 13).

1.4. Oito em cada dez municípios paulistas têm até 52 mil habitantes; dos maranhenses, até 33 mil; do Sudeste,
até 37 mil; do Nordeste, até 30 mil. Metade dos municípios paulistas tem até 13 mil habitantes
(`docs/tabelas/acumulado_populacao_2022.csv`). O território que esses municípios administram está em 15.6.

Figuras: `01_mapa_populacao_SP_MA`, `02_acumulado_populacao_*`, `03_peso_dos_pequenos_*`.

## 2. A maior fatia da receita (o mapa pintado)

Na conta principal (o que entrou no caixa, já sem os 20% que vão para o FUNDEB):

| Maior fatia | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| FPM | 53,2% | 7,0% | 65,0% | 46,6% |
| FUNDEB | 1,3% | 89,3% | 1,7% | 46,5% |
| ICMS e IPVA | 23,4% | 2,3% | 14,1% | 2,6% |
| Tributos próprios | 21,2% | 0,5% | 10,8% | 1,7% |
| Royalties | 0,3% | 0,0% | 3,2% | 0,3% |

Na outra conta (FPM e ICMS brutos, FUNDEB só pelo saldo entre o recebido e o aportado):

| Maior fatia | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| FPM | 55,3% | 35,3% | 67,9% | 75,3% |
| FUNDEB | 0,0% | 60,0% | 0,1% | 17,5% |

2.1. São Paulo fica em mosaico: FPM no oeste e no Vale do Ribeira (o interior profundo), ICMS onde há usina, indústria ou refinaria,
tributos próprios na Grande São Paulo, em Campinas e no litoral. O Maranhão fica quase todo de uma cor só, a do
FUNDEB, com ICMS no sul da soja (Balsas, Tasso Fragoso).

2.2. Por estado, o FPM é a maior fonte em 82% dos municípios de Minas, 78% do Rio Grande do Norte, 74% da
Paraíba, 63% de Pernambuco e de Sergipe, 53% de São Paulo, 51% do Piauí, 45% do Espírito Santo, 44% da Bahia,
28% do Ceará, 17% de Alagoas, 7% do Maranhão e 5% do Rio de Janeiro, onde os royalties lideram em 46%.

2.3. A ordem entre as regiões depende da contabilidade. Na conta principal, o FPM lidera em 18,4 pontos
percentuais a mais de municípios no Sudeste que no Nordeste (teste C1). Com o FUNDEB pelo saldo, lidera em 7,5
pontos a mais no Nordeste (teste Cb1). O que não muda: em São Paulo o FUNDEB quase não lidera (1,3% e 0,0%), e
no Maranhão lidera na maioria (89% e 60%). A semelhança de Minas, Rio Grande do Norte, Paraíba e Piauí com o
interior paulista é da conta principal.

2.4. O mapa joga fora mais da metade da pizza. Onde a maior fatia tem 31% e a segunda 30%, o município aparece
de uma cor só. A coluna `folga_maior` da base diz por quanto a maior fatia venceu.

2.5. Três receitas de uma vez só mexem em casos isolados: o precatório do antigo FUNDEF, que cai em "outras
transferências" (R$ 1,4 bilhão em 159 municípios, quase todos do Nordeste); a outorga de concessão de
saneamento em Alagoas e no Rio; e transferência de capital fora do comum, como em Biquinhas/MG, que recebeu
R$ 43,6 milhões do estado em 2024, 59% da receita-base (R$ 30,8 mil por habitante). Seis municípios têm uma só
categoria de capital acima de 25% da receita (coluna `alerta_capital_excepcional`).

2.6. A fatia "SUS" é só o repasse fundo a fundo corrente. O SUS de convênio e de capital (R$ 3,493 bilhões em
2.339 municípios, contando os convênios de capital, contas 2.4.1.4.50 e 2.4.2.2.50) fica em "outras
transferências" (`docs/METODO.md`).

2.7. Na média de 2023 a 2025, no painel de 830 municípios de São Paulo e do Maranhão com contas utilizáveis
nos três anos, o resultado é o mesmo: FPM em 52,2% dos paulistas, FUNDEB em 90,1% dos maranhenses.

Figuras: `05_mapa_maior_fatia_SP_MA`, `05_mapa_maior_fatia_sensibilidade_SP_MA`, `11_mapa_maior_fatia_SE_NE`,
`12_placar_maior_fatia_por_uf`, `04_composicao_receita_*`.

## 3. Dependência em parcela da receita

Mediana da parcela externa da receita (as seis fontes que a União e o estado repassam):

| Habitantes | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| até 5 mil | 90,2% | 96,5% (5 municípios) | 92,2% | 94,6% |
| 5 a 10 mil | 85,9% | 95,4% | 88,7% | 94,2% |
| 10 a 20 mil | 81,5% | 94,4% | 86,0% | 93,3% |
| 20 a 50 mil | 76,7% | 93,8% | 79,5% | 91,7% |
| 50 a 100 mil | 68,2% | 89,8% | 70,7% | 86,5% |

3.1. A tamanho igual, o Maranhão depende mais que São Paulo: 13,5 pontos a mais até 50 mil habitantes
(intervalo de 12,6 a 14,3). O número é coeficiente de regressão, e a comparação entre os dois estados é
exploratória, porque a hipótese foi ajustada vendo o dado deles. O teste que vale é o regional: o Nordeste
depende 6,7 pontos a mais que o Sudeste (6,3 a 7,1). Vale nas duas contabilidades, com erro agrupado por
estado, sem Minas, na mediana (testes A1 e A1b) e sem os 100 municípios com alerta de FPM ou de FUNDEB (13,4 e
6,7 pontos, família S). Na média de 2023 a 2025, São Paulo contra Maranhão dá 13,6 pontos (12,8 a 14,5); nos
mesmos 671 municípios em 2024, 13,5.

3.2. A distância cresce com o tamanho. No município minúsculo as duas regiões quase se encontram (92% e 95%).
Entre Sudeste e Nordeste são 4,9 pontos de 5 a 10 mil habitantes, 6,6 de 10 a 20 mil e 10,9 de 20 a 50 mil. O
município do Sudeste ganha base própria quando cresce; o do Nordeste, bem menos.

3.3. Tributo próprio: na mediana, 7,4% da receita no paulista de até 5 mil habitantes e 3,6% no nordestino.
Tirando o imposto de renda retido da folha da própria prefeitura, 5,4% e 1,6%. Na mediana dos municípios
pequenos do Nordeste, metade do "tributo próprio" é esse imposto de renda retido.

3.4. A diferença entre SP e MA não é efeito de tamanho. Dando a São Paulo a mistura de tamanhos do Maranhão, a
média paulista quase não muda (78,2% para 78,3%); os 15 pontos de distância vêm de dentro de cada faixa. Até
50 mil habitantes a mistura de tamanhos esconde parte da distância: a diferença observada entre as médias é
de 10,8 pontos e, a tamanho igual, de 13,5. Pondo o PIB por habitante na regressão, o coeficiente cai de 13,5
para 10,3 pontos entre os dois estados e de 6,7 para 3,2 entre as regiões. Isso descreve o mecanismo (receita
própria nasce da economia local); não é um viés a descontar.

Figuras: `06_dependencia_*`, `09_dispersao_dependencia_*`, `13_dependencia_por_uf`.

## 4. Dependência em reais por habitante

Mediana das transferências por habitante:

| Habitantes | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| até 5 mil | R$ 9.236 | R$ 8.782 (5 municípios; ver 4.1) | R$ 8.859 | R$ 8.457 |
| 5 a 10 mil | R$ 5.913 | R$ 6.542 | R$ 5.785 | R$ 6.028 |
| 10 a 20 mil | R$ 5.047 | R$ 5.661 | R$ 4.881 | R$ 5.387 |
| 20 a 50 mil | R$ 4.265 | R$ 4.835 | R$ 4.314 | R$ 4.553 |

4.1. O efeito muda com o tamanho.

- Até 5 mil habitantes, Sudeste e Nordeste empatam: diferença de -0,6%, intervalo de -3,2% a +2,1%.
- Até 5 mil habitantes, São Paulo contra Maranhão não dá para dizer: cinco municípios maranhenses, diferença de
  -3,1% com intervalo de -18% a +15% em 2024, e de -1,5% (-17% a +16%) na média de 2023 a 2025. A mediana dos
  cinco balança: no triênio, em reais de 2025, R$ 9.781 em São Paulo e R$ 8.426 no Maranhão.
- De 5 a 50 mil habitantes, o município paulista recebe de 9% a 12% a menos que o maranhense. O teste
  registrado antes, único até 50 mil habitantes, dá -9,3% (-12,3% a -6,1%; teste B1). O teste só de 5 a 50 mil
  dá -11,6% (-14,4% a -8,7%; teste B1x), mas foi escrito depois de ver o dado. Na média de 2023 a 2025 dá -9,5%
  (-12,2% a -6,7%). Por faixa, a diferença de 5 a 10 mil habitantes (R$ 546) não se distingue de zero depois da
  correção para comparações múltiplas (p = 0,057).
- Entre as duas regiões a diferença de 5 a 50 mil habitantes (5% a favor do Nordeste) não se distingue de zero
  quando se leva em conta que municípios do mesmo estado se parecem; ela depende de Minas.

4.2. A resposta depende de como se conta:

| Transferências por habitante | SP | MA |
|---|---|---|
| Média dos municípios | R$ 5.925 | R$ 5.642 |
| Mediana dos municípios | R$ 5.123 | R$ 5.375 |
| Por morador (soma sobre soma) | R$ 3.194 | R$ 4.527 |

Na média por município São Paulo recebe mais, porque tem muito município minúsculo; na mediana e por morador,
recebe menos. O município do Sudeste de até 5 mil habitantes recebe cerca de R$ 3,5 mil a mais por habitante
que o nordestino de 10 a 20 mil, que é o tamanho mais comum lá (teste B3).

4.3. O que cai com o tamanho é forte: o FPM líquido por habitante vai de R$ 4.137 (paulista de até 5 mil) a
R$ 1.177 (20 a 50 mil). Borá, com 907 habitantes no Censo, recebeu R$ 17,5 milhões de FPM bruto em 2024.

4.4. A cota mínima do FPM vale 10% a mais em São Paulo que no Maranhão, porque a fatia de cada estado está
congelada desde 1990 (`docs/pesquisa/fpm.md`).

4.5. O mesmo valor em reais não quer dizer a mesma cesta de serviço. O estudo não mede necessidade de gasto
nem custo de prover serviço em cada lugar, e por isso não afirma paridade de serviço onde os reais por
habitante empatam. O valor por habitante usa a estimativa de população de 2024; o Censo 2022 só define a faixa
de tamanho.

Figuras: `06_dependencia_*`, `14_transferencias_por_habitante_por_uf`.

## 5. Por município ou por morador

| Municípios com mais de 80% de receita externa | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| Parcela dos municípios com contas utilizáveis | 53,8% | 97,7% | 70,1% | 93,2% |
| Parcela da população do estado ou da região que mora neles | 7,1% | 78,5% | 16,5% | 56,5% |
| Idem, só sobre a população dos municípios com contas utilizáveis | 7,1% | 78,7% | 16,6% | 57,8% |

5.1. É aqui que mora o mal-entendido. São 53,8% das 628 prefeituras paulistas com contas utilizáveis (338) e
97,7% das 215 maranhenses (210). Nas paulistas mora um paulista em cada catorze. No Maranhão, quase quatro em
cada cinco moradores. Somando tudo, a receita externa é 49% da receita dos municípios paulistas e 87% da dos
maranhenses. A versão anterior chamava de "população do estado" a conta feita só sobre os municípios com
contas utilizáveis (78,7% no Maranhão, 16,6% no Sudeste, 57,8% no Nordeste); sobre toda a população, os
números são os da segunda linha. A classe conta como dependência o FUNDEB e o SUS, que são receita externa
com destino obrigatório.

5.2. Contando todos os municípios, e supondo os de contas não utilizáveis todos abaixo ou todos acima do
corte, a parcela fica entre 52,4% e 55,0% dos 645 paulistas e entre 96,8% e 97,7% dos 217 maranhenses.

## 6. Verba negociada: emenda e convênio

Esta seção mudou nas duas rodadas de revisão cruzada. O que o estudo chamava de "transferências voluntárias"
tinha R$ 3,493 bilhões do SUS dentro, e a Lei de Responsabilidade Fiscal (art. 25) tira o SUS dessa categoria.
A medida principal passou a ser a restrita: convênios e transferências de capital, sem o SUS e sem o convênio
corrente estadual de educação, que pode ser repasse regular. A medida ampla, a de antes, fica como
sensibilidade. Nenhuma das duas é a "transferência voluntária" da lei (`docs/METODO.md`). Na rodada 2 saíram
da restrita os convênios de capital da saúde (2.4.1.4.50 e 2.4.2.2.50, R$ 435,4 milhões entre os municípios
com contas utilizáveis), que a primeira correção tinha deixado dentro (15.1). Os números abaixo já são os da
base refeita.

6.1. **Emenda federal.** Pagas em 2025 a prefeituras e fundos municipais (Portal da Transparência; o valor pago
inclui restos a pagar de anos anteriores), por habitante, mediana dos municípios de até 20 mil habitantes:
Sergipe R$ 670, Piauí R$ 622, Paraíba R$ 586, Rio de Janeiro R$ 518, Rio Grande do Norte R$ 493, Pernambuco
R$ 462, Alagoas R$ 454, Espírito Santo R$ 378, Maranhão R$ 357, Ceará R$ 294, Minas R$ 274, Bahia R$ 233, São
Paulo R$ 149. São Paulo é o último na mediana, na média e ponderando por população. Em parcela da receita de
2025: 1,8% em São Paulo, 5,2% no Maranhão, 7,9% no Piauí. Sobre a receita de 2024, que era o denominador da
versão anterior: 2,0%, 5,5% e 9,0%. Nos estados que faltavam: Minas 3,5%, Espírito Santo 5,0%, Rio 5,1%. Na
mediana das regiões, 6,0% no Nordeste e 2,9% no Sudeste. São Paulo é o último dos treze também nessa conta
(tabela em 15.3).

6.2. A tamanho igual, o Maranhão recebe R$ 240 a mais de emenda federal por habitante que São Paulo, e o
Nordeste R$ 235 a mais que o Sudeste (teste D3). É o que a regra produz: a cota é por parlamentar e por
bancada, e São Paulo tem um deputado federal para cada 634 mil habitantes; o Maranhão, um para cada 376 mil. O
arquivo só cobre prefeitura e fundo municipal; em São Paulo, um terço da emenda paga em 2025 a favorecidos do estado vai
para o governo estadual, para entidades e para empresas, e isso fica fora.

6.3. **Convênio e transferência de capital nas contas da prefeitura**, medida restrita, mediana dos municípios
de até 20 mil habitantes, em parcela da receita:

| De quem vem | SP | MA | Outros |
|---|---|---|---|
| União, restrita | 0,66% | 0,75% | Piauí 3,3%, Paraíba 3,9% |
| União, ampla | 0,74% | 0,90% | Piauí 3,9%, Paraíba 4,3% |
| Estado, restrita | 2,5% | 0,0% | Espírito Santo 6,0%, Minas 2,3%, Rio 0,0% |
| Estado, ampla | 4,2% | 0,0% | Espírito Santo 6,4%, Minas 3,3%, Rio 0,0% |

A tamanho igual, na medida restrita, o paulista tem 2,2 pontos a mais de verba estadual (2,0 a 2,5) e 0,9
ponto a menos de verba federal (0,5 a 1,3) que o maranhense (testes D1e e D1u). Na ampla, 4,4 pontos a mais e
1,0 a menos. Entre as regiões, o Sudeste tem 2,1 pontos a mais de verba estadual na restrita (1,9 a 2,3); a
diferença federal (1,2 ponto a favor do Nordeste, 1,0 a 1,4) não se distingue de zero com erro agrupado por
estado, nem depois da correção para vários testes (p = 0,058).

O 0,0% do Maranhão é mediana de lançamento, não prova de que o estado não repassa. Das 127 prefeituras
maranhenses de até 20 mil habitantes, 90 lançaram zero nessas contas (68 na medida ampla). Na média, a verba
estadual é 0,22% da receita no Maranhão e 3,07% em São Paulo (0,36% e 5,22% na ampla). Há uma segunda razão
possível para o zero, levantada pela pesquisa profunda do Gemini e sem fonte: obra paga direto pelo governo do
estado não passa pela conta da prefeitura. Fica como pergunta.

6.4. O que São Paulo tem de diferente é o governo do estado como fonte de verba negociada, e o tamanho disso
caiu com a medida restrita: de 4,2% para 2,5% da receita. No município paulista de até 5 mil habitantes, a
verba negociada (federal e estadual) equivale a 49% do investimento, e só a estadual a 35%. Na medida ampla
são 74% e 56%. Toda razão sobre o investimento herda a oscilação do investimento entre os anos (15.2).

6.5. Essa medida não enxerga a emenda. Cerca de dois terços da emenda paga a prefeituras e fundos municipais vão para o fundo
municipal de saúde (seis em cada dez reais nos municípios de até 20 mil habitantes) e entram na conta do SUS; e a
conta própria da emenda Pix registra 68% do valor pago em São Paulo e 24% no
Maranhão, onde o dinheiro aparece em "outras transferências da União". Para emenda, vale só o Portal.

6.6. O que falta medir: emenda de deputado estadual e convênio estadual por município e por programa. É a peça
que decide a versão "verba de deputado" da tese.

6.7. Na média de 2023 a 2025 (São Paulo e Maranhão, 671 municípios de até 50 mil habitantes) o resultado se
mantém: 2,0 pontos a mais de verba estadual em São Paulo (1,9 a 2,2) e 1,0 ponto a menos de verba federal (0,7
a 1,3), na medida restrita. O convênio federal de 2024 ficou abaixo do de 2023 e perto do de 2025: mediana dos
municípios de até 20 mil habitantes de 0,94%, 0,66% e 0,59% em São Paulo; 1,21%, 0,75% e 0,95% no Maranhão.
Entre as regiões o triênio dá o mesmo que 2024: 1,2 ponto a mais de verba federal no Nordeste e 2,1 pontos a
mais de verba estadual no Sudeste. A versão anterior dizia que 2024 "foi fraco de convênio federal" porque
comparava a mediana de um ano (0,66% e 0,75%) com a mediana da média de três anos (0,87% e 1,45% na base
refeita). Convênio entra em pacote, num ano sim e noutro não; a média de três anos tira os zeros e sobe
sozinha. A frase saiu.

Figuras: `16_emendas_por_habitante_por_uf`, `17_voluntarias_da_uniao_por_uf`, `18_voluntarias_do_estado_por_uf`,
`08_voluntarias_*` (as três últimas agora na medida restrita).

## 7. Custo da máquina

7.1. Câmara e administração (funções 01 e 04) custam, por habitante, de duas a três vezes mais no município de
até 5 mil habitantes que no de 20 a 50 mil: R$ 1.764 contra R$ 618 em São Paulo, R$ 1.520 contra R$ 648 no
Sudeste, R$ 1.788 contra R$ 613 no Nordeste.

7.2. A economia de escala é forte no município minúsculo e se esgota perto de 20 mil habitantes. A elasticidade
do gasto por habitante em relação à população é de -0,91 até 5 mil habitantes (dobrar a população corta o
gasto por habitante quase pela metade), -0,40 de 5 a 20 mil e -0,07 de 20 a 100 mil, que não se distingue de
zero (teste E1 por trecho). Essas elasticidades são das duas regiões juntas e foram estimadas depois de ver a
curva. O número único, registrado antes, é de -0,28 para todos os tamanhos e de -0,23 só em São Paulo; ele
esconde a curva.

7.3. Entre regiões não há diferença estável a tamanho igual: -2% na média (indistinguível de zero) e -7% na
mediana, com o Sudeste abaixo. E a medida não é comparável entre estados: fora de São Paulo, a administração
da saúde e da educação costuma ser lançada dentro dessas funções (subfunção 122), não na função 04. Somando a
subfunção 122 de todas as funções, o Maranhão fica bem acima de São Paulo. A função 01 mais a 04 é um piso; a
medida ampliada é um teto.

7.4. Os tributos próprios não pagam a Câmara e a administração em 91% dos municípios paulistas de até 5 mil
habitantes, em 64% dos de 5 a 10 mil e em 13% dos de 20 a 50 mil. No Maranhão, em 96% de todos os municípios,
e ainda em 83% dos de 50 a 100 mil habitantes. Essa conta inclui o imposto de renda retido na fonte como
tributo próprio. Sem ele: 96%, 77% e 25% em São Paulo; 98% e 92% no Maranhão.

7.5. Simulação do critério da PEC 188/2019 (menos de 5 mil habitantes e IPTU, ITBI e ISS abaixo de 10% da receita),
na leitura da CNM, que usou a receita corrente líquida como denominador, sobre as contas de 2024: 242
municípios em Minas, 133 em São Paulo, 83 no Piauí, 68 na Paraíba, 49 no Rio Grande do Norte e 5 no Maranhão.
A contagem usa todas as contas em que o critério é calculável, não só as utilizáveis: 616 municípios nos 13
estados, 594 entre os de contas utilizáveis (São Paulo: 133 e 121; Maranhão: 5 e 5). Fica perto da lista da
CNM de 2019 (223, 135, 75, 68, 48 e 4). A PEC foi arquivada em 22/12/2022, sem votação; não há proposta em
tramitação com esse critério. O texto do artigo, por duas transcrições secundárias iguais (o PDF do Senado não
foi aberto), dizia "incorporado": o município de até 5 mil habitantes que não comprovasse, até 30/06/2023,
impostos próprios de ao menos 10% da receita seria incorporado a um vizinho a partir de 1º/01/2025. Os títulos
de 5 a 7/11/2019 disseram "extinguir", "extintas", "extinção" e "tirar do mapa".

Figuras: `07_custo_da_maquina_*`, `15_criterio_pec188_por_uf`.

## 8. FUNDEB: quem paga e quem recebe

8.1. 93% dos municípios paulistas de até 5 mil habitantes são doadores líquidos do FUNDEB: aportam 20% de um
FPM e de um ICMS grandes para o tamanho deles e têm poucos alunos. No Sudeste, 91%. No Nordeste, 21% na mesma
faixa e 1% de 5 a 50 mil habitantes. No Maranhão, nenhum dos cinco, que são todos os municípios do estado
nessa faixa. O resultado resiste a tirar os 62 municípios com aporte a mais de 2 pontos do esperado (coluna
`alerta_fundeb`, 27 deles no Piauí): 93% em São Paulo, 91% no Sudeste e 22% no Nordeste.

8.2. Não é dinheiro que sai de São Paulo para o Maranhão: são 27 fundos, um por estado. Dentro do fundo
paulista o município minúsculo perde para os que têm mais alunos; dentro do maranhense todos os municípios
ganham, do governo do estado e da complementação da União. O resultado é uma diferença de natureza: o dinheiro
de fora do município pequeno paulista é livre (FPM e ICMS); o do maranhense é carimbado para a educação. As
contas anuais não separam os três tipos de complementação da União.

## 9. Saúde fiscal

A CAPAG mede capacidade de pagamento (endividamento, poupança corrente e liquidez). Não mede autonomia: um
município pode viver de transferência e ter nota A.

9.1. Na CAPAG do Tesouro (posição de 01/09/2026), distribuição sobre todos os municípios de cada grupo:

| Nota | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| A ou A+ | 22,0% | 14,3% | 25,1% | 9,6% |
| B ou B+ | 13,5% | 18,4% | 18,8% | 21,6% |
| C | 60,2% | 56,7% | 47,9% | 55,6% |
| D | 0,2% | 0,0% | 0,1% | 1,0% |
| Sem nota | 4,2% | 10,6% | 8,2% | 12,2% |

Entre os que têm nota, a C aparece em 63% dos paulistas e em 63% dos maranhenses; no Sudeste, 52%; no Nordeste,
63%. Na nota C os dois estados empatam; no topo São Paulo está melhor (A ou A+ em 23% dos que têm nota, contra
16% no Maranhão). O Espírito Santo (19% com C) e Minas (45%) puxam o Sudeste.

9.2. No IFGF Autonomia da Firjan, que conta a cota-parte do ICMS como receita local, a mediana paulista bate no
teto do índice (1,00) e a maranhense no piso (0,00). Nos paulistas de até 10 mil habitantes a mediana é 0,7; nos
do Sudeste, 0,3.

## 10. Os degraus do FPM

10.1. A população publicada se concentra logo acima dos degraus de faixa do FPM. No Censo 2022, no país,
somando os 17 degraus, 546 municípios estão até 2% acima de um degrau e 189 até 2% abaixo (74% acima; o acaso
daria perto de 50%). Só no degrau de 10.188 habitantes são 104 acima e 20 abaixo. No Censo 2010 o padrão é o
mesmo (479 e 157). O excesso resiste a janela fixa em habitantes, não aparece em degraus falsos deslocados e
existe nas cinco regiões (teste F1, binomial, e `revisao/claude/testes.md`).

10.2. A soma não quer dizer que cada degrau tenha excesso. O GPT rodou um teste de densidade degrau a degrau
(`rddensity`, de Cattaneo, Jansson e Ma; `revisao/gpt/PARCIAL-TEMPO.md`, seção 6; não refeito por mim, o pacote
não está no ambiente do projeto). Com correção para 17 comparações, ele rejeita a continuidade em quatro
degraus no Censo 2022 (10.188, 13.584, 16.980 e 23.772 habitantes) e em cinco no Censo 2010 (os mesmos e
30.564). Em 10.188, a densidade logo acima é 4,82 vezes a de logo abaixo em 2022 e 7,45 vezes em 2010. Cinco
degraus têm municípios de menos para testar.

10.3. Nas estimativas de 2024 a 2026 o excesso não some: ele anda. A estimativa é o Censo multiplicado por um
fator de crescimento, então quem estava até 2% acima do degrau em 2022 aparece de 2% a 5% acima em 2024.

10.4. Eu esperava não achar isso no Censo 2022 e estava errado. O dado mostra a concentração; não mede a
causa. Causas possíveis, sem escolher uma:

- esforço de coleta e contestação de quem ficaria logo abaixo do degrau;
- decisão judicial que fixa população acima da do Censo (reportagem do Valor de 22/02/2026, citada pelo Grok;
  não aberta por mim);
- população usada pelo TCU diferente da do Censo final: o GPT achou 111 municípios nessa situação entre os do
  estudo, 13 deles perto do primeiro degrau, e não atribuiu a diferença a decisão judicial sem olhar caso a
  caso;
- a literatura já tinha apontado o padrão no Censo 2010 (Monasterio, 2013).

Falta medir quanto cada causa pesa. Um complicador: abaixo do primeiro degrau, 53,6% dos municípios têm o
coeficiente protegido pela LC 198/2023, contra 4,5% acima (conta do GPT), então subir de faixa hoje muda pouco
o coeficiente efetivo. A lei mantém o coeficiente de quem perdeu população no Censo e o reduz aos poucos: 10%
da perda no primeiro exercício, mais 10 pontos por ano, até 90% no nono; no décimo volta a regra geral. Para
este estudo, o recado é que perto dos degraus a população não é uma medida neutra do tamanho.

10.5. A literatura dos degraus já registra a quebra nos anos de Censo e a contorna usando as estimativas
anuais (Corbi, Papaioannou e Surico, 2019; Litschig, 2012). Corbi e coautores acham manipulação nos anos de
Censo e de contagem, refazem as contas sem esses anos e o resultado quase não muda. Litschig documenta a quebra
nas estimativas usadas no FPM de 1991. Brollo e coautores (2013) e Litschig e Morrison (2013) testam a
densidade e não acham quebra nas populações que usam. O achado desta seção é de Censo e é coerente com eles.
O mesmo artigo de Corbi mede multiplicador local de renda perto de 2 para o FPM (de 1,7 a 2,5): tirar FPM do
município pequeno tem custo local de renda e de emprego que a conta contábil deste estudo não mede.

## 11. Evolução de 2002 a 2025

Série do IPEADATA, receita bruta, que tem os mesmos totais das contas anuais. A "dependência" desta série é
transferência corrente sobre receita corrente bruta. Não é a mesma variável da seção 3, que é líquida das
deduções e sem a previdência própria; os níveis não se comparam. Municípios de até 20 mil habitantes. As colunas de 2002 e de 2025 são a
mediana dos municípios de cada ano, a mesma do deck e do e-book; a mudança é a mediana da variação dentro dos
que aparecem nos dois anos (teste G):

| | 2002 | 2025 | Mudança (pontos) |
|---|---|---|---|
| Transferências correntes sobre a receita corrente, SP | 89,1% | 86,3% | -2,7 |
| Idem, MA | 97,7% | 94,7% | -3,2 |
| Idem, Sudeste | 92,3% | 88,7% | -3,1 |
| Idem, Nordeste | 96,7% | 93,0% | -3,4 |
| FPM sobre a receita corrente, SP | 37,5% | 35,5% | -1,6 |
| Idem, MA | 52,5% | 29,0% | -23,2 |
| Idem, Sudeste | 49,7% | 40,9% | -6,5 |
| Idem, Nordeste | 52,5% | 36,1% | -16,1 |
| Cota-parte do ICMS sobre a receita corrente, SP | 26,2% | 20,9% | -5,4 |
| Idem, MA | 4,6% | 9,2% | +4,9 |
| Câmara e administração sobre a receita corrente, SP | 18,3% | 13,1% | -4,6 |
| Idem, MA | 20,7% | 14,4% | -6,7 |

11.1. A dependência quase não se mexeu. De 2002 a 2021 a mediana caiu cerca de um ponto; os outros dois ou três
vieram depois de 2021, e a maior parte não é imposto próprio. Segundo a conta do GPT (não refeita por mim: a
série longa não traz essa conta), de 2021 para 2022, nos municípios de até 10 mil habitantes, a dependência
caiu 1,4 ponto nos dois estados e o rendimento financeiro subiu 1,4 ponto da receita em São Paulo e 0,6 no
Maranhão. A conta de rendimento explica a queda em São Paulo e menos da metade no Maranhão. Que a causa seja o
juro alto segue hipótese. A distância entre São Paulo e o Maranhão é a de 2002 (cerca de 8,5 pontos: 8,6 em 2002 e 8,5 em 2025).

11.2. A série começa em 2002 de propósito. Até 2001 o imposto de renda retido na fonte entrava como
transferência e a função Administração tinha outra classificação; comparar com 2000 fabrica queda.

11.3. O peso do FPM caiu muito mais no Nordeste (16 pontos) que no Sudeste (6,5), e no Maranhão caiu quase à
metade, com o FUNDEB e o ICMS ocupando o lugar: é troca de uma transferência por outra, não ganho de base
própria. Em São Paulo o FPM desceu até 2020 e voltou: hoje pesa quase o mesmo que em 2002. Parte da volta é
regra: a Emenda Constitucional 112/2021 acrescentou ao FPM 0,25% da arrecadação do imposto de renda e do IPI em
2022 e 2023, 0,5% em 2024 e 1% a partir de 2025. O fundo passou de 24,75% dessa arrecadação em 2022 para 25,5%
em 2025, cerca de 3% a mais só pela regra. O Sudeste pequeno só passou à frente do Nordeste em 2023 e 2024, e
por causa de Minas; o município pequeno paulista está no nível do nordestino.

11.4. A cota-parte do ICMS perdeu um quinto do peso no município pequeno paulista (de 26% para 21% da receita
corrente) e dobrou no maranhense. É a fonte que mais distingue o interior paulista do nordestino, e a distância
está encolhendo. No Maranhão a regra de rateio mudou dentro do período (Lei estadual 11.815/2022, com repasse
pela regra nova desde 2024, segundo o Grok; lei não aberta por mim), e em São Paulo também.

11.5. O peso da Câmara e da administração na receita corrente caiu em todo lugar, 5 a 7 pontos, sem diferença
entre Sudeste e Nordeste. No Maranhão a série oscila muito (mínimo de 14% em 2012).

11.6. Por estado, a ordem da dependência quase não mudou em 23 anos: Maranhão, Paraíba, Bahia e Piauí no topo;
São Paulo e Rio de Janeiro no fim.

11.7. O ano de 2024 não é exceção. No painel conta a conta de 2022 a 2025, com a mesma receita líquida do
retrato, a dependência do município de até 10 mil habitantes ficou entre 87,1% e 88,3% em São Paulo e entre
95,2% e 95,7% no Maranhão. O peso do FPM subiu de 33,6% para 36,0% no paulista e caiu de 30,3% para 27,3% no
maranhense; a EC 112/2021 explica parte da subida paulista. Nos 13 estados é igual: de 2022 a 2025 a
dependência do município de até 10 mil habitantes ficou entre 90,0% e 90,9% no Sudeste (90,9%; 90,0%; 90,7%;
90,1%) e entre 94,0% e 94,9% no Nordeste (94,9%; 94,7%; 94,4%; 94,0%). O peso do FPM ficou parado no Sudeste
(38,1% para 38,6%) e caiu no Nordeste (39,2% para 34,1%). A base tem os 13 estados nos quatro anos desde a
rodada 2: 3.352, 3.360, 3.356 e 3.371 municípios com contas utilizáveis.

11.8. **Triênio 2023 a 2025.** O GPT refez as comparações entre São Paulo e Maranhão com a média de três anos,
em reais de 2025, no painel de 830 municípios com contas utilizáveis nos três anos (617 paulistas e 213
maranhenses). Eu refiz com as bases remontadas e os números batem:

| Comparação, São Paulo contra Maranhão | Só 2024 | Média de 2023 a 2025 |
|---|---|---|
| Dependência a tamanho igual, até 50 mil hab. (pontos a mais no MA) | 13,5 | 13,6 (12,8 a 14,5) |
| Transferências por habitante, 5 a 50 mil hab. (SP em relação ao MA) | -11,6% | -9,5% (-12,2% a -6,7%) |
| Idem, até 5 mil hab. | -3,1% | -1,5% (-16,6% a +16,3%) |
| FPM como maior fatia em SP; FUNDEB no MA | 53,2%; 89,3% | 52,2%; 90,1% |
| Verba estadual, medida restrita, até 50 mil hab. (pontos a mais em SP) | 2,2 | 2,0 (1,9 a 2,2) |
| Verba federal, medida restrita (pontos a menos em SP) | 0,9 | 1,0 (0,7 a 1,3) |

As conclusões entre os dois estados não dependem do ano. Serve como faixa, não como número novo: 2023 e 2025
não passaram pela mesma conferência de 2024. O investimento mediano por habitante em São Paulo, em reais de
2025, foi de R$ 640 em 2023, R$ 565 em 2024 e R$ 376 em 2025: 2024 não aparece como pico.

**Entre as regiões o triênio também não muda o retrato.** No painel de 3.261 municípios utilizáveis nos três
anos, o Nordeste depende 7,1 pontos a mais que o Sudeste a tamanho igual (6,7 a 7,5; com erro agrupado por
estado, 3,5 a 10,8), contra 6,7 só com 2024. O FPM é a maior fatia em 65,1% dos municípios do Sudeste e 46,8%
dos do Nordeste (65,0% e 46,6% em 2024). As transferências por habitante empatam: +0,8% até 5 mil habitantes e
-3,5% de 5 a 50 mil, sem distinguir de zero com erro agrupado. A verba federal (1,2 ponto a mais no Nordeste),
a estadual (2,1 a mais no Sudeste) e o custo da máquina (elasticidade de -0,28) ficam iguais. O ano de 2024
pesa no investimento: no Nordeste é o pico dos três anos (R$ 347, R$ 507 e R$ 421 por habitante na faixa de 10
a 20 mil, em reais de 2025); no Sudeste, 2024 repete 2023 e 2025 cai um terço. Sergipe é o estado em que 2024
foge: receita própria de uma vez só baixou a dependência mediana de 91% para 85%. A conta inteira está em 15.2.

Figuras: `21_` a `29_` (painel de 2022 a 2025, SP e MA; as `21_` a `27_` existem também com final `_SE_NE`,
para as regiões), `41_` a `49_` (série longa, de 2000 a 2025, sem 2008)
e `31_` a `33_` (IFGF, 2013 a 2024). Cada painel
traz a mediana, as manchas de P25 a P75 e de P10 a P90, os municípios fora da cerca de Tukey e a contagem deles
por ano; as mesmas contas estão em `docs/tabelas/`.

## 12. O interior paulista por região

| Região intermediária | Municípios | Habitantes (mediana) | FPM é a maior fatia | Transferências sobre a receita (mediana) | Idem, só de 5 a 10 mil hab. (municípios) |
|---|---|---|---|---|---|
| Presidente Prudente | 55 | 7.085 | 76,4% | 87,3% | 87,8% (10) |
| Marília | 54 | 6.383 | 64,8% | 87,1% | 86,8% (12) |
| Araçatuba | 41 | 5.519 | 68,3% | 85,6% | 84,2% (10) |
| São José do Rio Preto | 87 | 6.867 | 67,8% | 85,4% | 85,4% (25) |
| Sorocaba | 78 | 18.268 | 51,3% | 83,1% | 85,3% (14) |
| Bauru | 48 | 11.235 | 62,5% | 82,9% | 85,9% (9) |
| Ribeirão Preto | 63 | 16.818 | 44,4% | 80,0% | 85,3% (15) |
| Araraquara | 26 | 15.459 | 46,2% | 77,3% | 83,5% (5) |
| São José dos Campos | 39 | 13.975 | 56,4% | 76,5% | 87,4% (8) |
| Campinas | 87 | 31.328 | 35,6% | 72,3% | 76,9% (11) |
| São Paulo | 50 | 149.477 | 14,0% | 65,6% | nenhum |

12.1. As quatro regiões de cima são as do oeste do estado e são as de município menor: o município mediano tem
de 5 a 7 mil habitantes e 85% a 87% da receita vem de transferência. Nenhuma região do Maranhão fica abaixo de
92%.

12.2. A tamanho igual, o oeste não se separa do resto. Olhando só os municípios de 5 a 10 mil habitantes, nove
das dez regiões ficam entre 83% e 88%; só Campinas fica abaixo (77%). Na regressão com a população, as quatro
regiões do oeste dependem 0,9 ponto a mais que o resto do estado, com intervalo de -0,2 a +2,0, que não se
distingue de zero (teste R1). O "interior profundo" paulista tem endereço porque é lá que estão os municípios
pequenos, não porque o oeste dependa mais que um município do mesmo tamanho em outra região.

## 13. Dependência como classe única

A pergunta do dono: e se dependência fosse uma classe só, binária (depende ou não depende)? Existe corte em que
a fração de municípios dependentes se iguala entre os estados?

Parcela dos municípios com contas utilizáveis em que as transferências passam do corte:

| Corte | SP, todos | MA, todos | SP, até 20 mil hab. | MA, até 20 mil hab. | SP, até 5 mil hab. | MA, até 5 mil hab. |
|---|---|---|---|---|---|---|
| 50% | 96,8% | 100,0% | 100,0% | 100,0% | 100,0% | 100,0% |
| 60% | 90,1% | 100,0% | 99,7% | 100,0% | 100,0% | 100,0% |
| 70% | 78,0% | 99,5% | 97,9% | 100,0% | 99,3% | 100,0% |
| 80% | 53,8% | 97,7% | 82,2% | 98,4% | 96,4% | 100,0% |
| 90% | 14,6% | 85,6% | 24,2% | 94,5% | 52,9% | 100,0% |
| 95% | 0,6% | 36,3% | 1,1% | 46,5% | 2,9% | 80,0% |

Entre as regiões:

| Corte | Sudeste, todos | Nordeste, todos | Sudeste, até 20 mil hab. | Nordeste, até 20 mil hab. | Sudeste, até 5 mil hab. | Nordeste, até 5 mil hab. |
|---|---|---|---|---|---|---|
| 50% | 98,5% | 99,8% | 100,0% | 99,9% | 100,0% | 100,0% |
| 60% | 95,0% | 99,1% | 99,6% | 99,6% | 99,7% | 100,0% |
| 70% | 87,9% | 97,8% | 98,4% | 99,2% | 99,5% | 99,6% |
| 80% | 70,1% | 93,2% | 90,6% | 97,6% | 97,6% | 99,6% |
| 90% | 31,7% | 72,3% | 45,9% | 83,7% | 70,7% | 88,7% |
| 95% | 2,7% | 21,5% | 4,0% | 29,2% | 8,4% | 43,5% |

A tabela completa, com população, a faixa de até 10.188 habitantes e os limites para os municípios excluídos,
está em `docs/NUMEROS.md`.

13.1. Há igualdade, mas só nas pontas da curva. No conjunto de todos os municípios, nos cortes de 50% a 100%,
as frações de São Paulo e do Maranhão só se igualam em zero, com corte acima de 99,8%. Abaixo de 26,3% as duas
são 100% (conta do GPT, não refeita aqui). Entre os municípios de até 20 mil habitantes, as
duas são 100% com qualquer corte até 50,1%; até 10.188 habitantes, com qualquer corte até 62,5%; até 5 mil
habitantes, com qualquer corte até 66,0%. Esses limites são a menor dependência entre os paulistas de cada
recorte. Daí para cima a fração paulista cai e a maranhense não, e as curvas não se cruzam de novo antes de
zerar.

13.2. Essa igualdade é vazia de conteúdo. Ela diz que todo município pequeno dos dois estados recebe mais da
metade da receita de fora. Isso vale para quase todo município pequeno do país e é desenho do federalismo
fiscal brasileiro: o imposto se arrecada onde está a atividade econômica e se redistribui por fórmula. Uma
classe em que cabem todos não separa ninguém. Assim que o corte passa a separar, separa a favor da tese
contrária: com 80%, 82% dos paulistas e 98% dos maranhenses de até 20 mil habitantes; com 90%, 24% e 94%.

13.3. Entre as regiões, nos municípios de até 20 mil habitantes, as duas curvas são praticamente iguais com
cortes de 50% a 61%: a diferença alterna de -0,02 a +0,26 ponto (conta do GPT, não refeita aqui). É questão de
um ou dois municípios nordestinos com dependência baixa, e as duas frações estão acima de 99,5%. Não é
resultado.

13.4. A classe única joga fora a informação que distingue os dois estados: a distância dentro da classe. Um
município com 81% e outro com 97% ficam no mesmo lado do corte de 80%. Por isso o estudo trabalha com a
parcela contínua (seção 3), com reais por habitante (seção 4) e com a população que mora nos municípios
dependentes (seção 5).

Figuras: `19_corte_dependencia_SP_MA`, `19_corte_dependencia_SE_NE`.

## 14. O que a segunda rodada de pesquisa acrescenta

Sete frentes documentais de 05 e 06/10/2026, cada uma com arquivo próprio em `docs/pesquisa/` e as marcas do que
foi conferido na fonte. O texto corrido está no relatório (`relatorio/relatorio.md`, Partes II e III). Aqui fica
só o que muda a leitura dos achados acima.

14.1. **A malha tem história** (`referencias-base.md`; relatório, seção 11). De 1988 a 2000 São Paulo criou 73
municípios, 51 com menos de 5 mil habitantes; o Maranhão criou 85, e só 12 eram desse tamanho (Tomio, 2002,
p. 64). Os pequenos municípios criados depois de 1988 levam 4,4% do FPM do interior paulista e 8,7% do
maranhense (Brandt, 2010, p. 67). Isso explica o 150 contra 5 da seção 1 e diz que a maior parte dos
micromunicípios paulistas é anterior a 1988. O piso legal não explica por que os novos municípios maranhenses
nasceram maiores: os dois estados exigiam 1.000 eleitores (15.7).

14.2. **Tamanho, custo e escala** (`escala-urbana.md`; seção 12). A pergunta do dono: a população é variável
substituta das outras, ou são coisas separadas? Os expoentes do logaritmo de cada grandeza contra o da
população, nos 3.356 municípios: PIB 1,14; tributos próprios 1,22; ISS 1,27; IPTU 1,68; FPM 0,52;
transferências 0,77; Câmara e administração 0,75. A economia só cresce mais que a população acima de uns 50 mil
habitantes (até aí o expoente do PIB é 1,01). A máquina é custo fixo: expoente 0,14 até 5 mil habitantes e 0,98
acima de 50 mil. Um FPM proporcional à população dentro de cada estado explicaria 67% do excesso de
transferências por habitante do município minúsculo e 21% da queda da dependência em parcela da receita. Tamanho
não fecha a conta entre os dois estados: dos 14,8 pontos de distância (843 municípios, todos os tamanhos),
sobram 11,9 com população e PIB por habitante. Limite: município não é cidade, e expoente de corte transversal
não é lei.

14.3. **A emenda segue a cadeira** (`representacao.md`; seção 13). O nome técnico é desproporcionalidade da
representação (*malapportionment*). Pelo índice de Loosemore-Hanby com o Censo 2022, 10,4% na Câmara e 37,3% no
Senado (conta própria; as cadeiras por estado foram conferidas em 06/10/2026 na página da Câmara dos Deputados:
27 de 27 bancadas, soma 513). Para 1998, Samuels e Snyder (2001, p. 660 a 662) dão 0,0913 na Câmara e 0,4039 no
Senado, o segundo mais desproporcional da lista deles. Razão entre cadeiras
e população na Câmara: Norte 1,48; Nordeste 1,09; Sudeste 0,84. A São Paulo faltam 42 cadeiras. Pela regra de
2025, a emenda dá R$ 73 por habitante em São Paulo, R$ 193 no Maranhão e R$ 1.463 em Roraima, e essa ordem tem
correlação de 0,81 com a mediana municipal da seção 6. A sobrerrepresentação é do Norte de estados pequenos e do
Senado, não do Nordeste como bloco. O gráfico dessa conta tem um ponto por estado, não por município.

14.4. **Emendas no tempo** (`emendas-linha-do-tempo.md`; seção 14). A preços de 2025, o empenhado foi de R$ 17,5
bilhões em 2018 para R$ 47,1 bilhões em 2025. A transferência especial ("emenda Pix") foi de R$ 0,8 bilhão em
2020 para R$ 8,1 bilhões em 2024. A série do Portal da Transparência só serve de 2018 em diante, e 2026 é
parcial. O ano da série é o do orçamento da emenda. O valor pago que o deck mostra soma o que foi pago depois
como restos a pagar: R$ 15,6 bilhões nas emendas do orçamento de 2018 e R$ 41,4 bilhões nas do de 2024 (2,7
vezes). Pelo ano do pagamento, R$ 18,7 bilhões em 2018 e R$ 41,2 bilhões em 2024 (2,2 vezes). A alta resiste nos
dois critérios. A série pelo ano do pagamento, por tipo, não foi montada. O orçamento de 2026 (Lei 15.346,
publicada em 14/01/2026, por fonte secundária) traz cerca de R$ 61 bilhões em emendas: R$ 26,6 bilhões
individuais, R$ 11,2 bilhões de bancada, R$ 12,1 bilhões de comissão e R$ 11,1 bilhões acolhidos na programação
dos ministérios (Agência Senado, 19/12/2025).

14.5. **A nota técnica do CEM** (`cem-nt23.md`; seção 15). O par R$ 1.816 contra R$ 393 por habitante soma só FPM
e FUNDEB. A nota nega propor fusão de municípios (p. 4) e não tem dado de emenda. Na base de 2024, por morador:
a União manda 3,3 vezes mais ao município de até 31 mil habitantes que ao de mais de 175 mil, e a emenda é 6,5
vezes maior; na receita-base do estudo, R$ 6.373 contra R$ 5.623 por morador, 13% a mais (com toda a receita
líquida, sem os cortes da receita-base, seriam R$ 6.545 contra R$ 6.178). A conta é em outro universo e com
outra definição que a da nota; não refuta a nota. Quem menos tem é o município grande do Nordeste: R$ 4.300 por
morador, contra R$ 6.118 no grande do Sudeste. A nota diz que a demanda não justifica a diferença. A nota não
mede demanda, e este estudo também não: a demanda continua sem medida, nos dois lados.

**Posição do autor.** "A demanda não justifica" é juízo de valor, não medida: a nota não mede demanda, e este
estudo também não. O autor defende o contrário. Para ele, o Estado pode e deve sustentar os municípios menores
e mais atrasados, porque o desenvolvimento deles beneficia a todos, e a proporção poderia ser até maior: os
municípios de até 50 mil habitantes administram 81% do território dos 13 estados, com 30% da população (15.6).

14.6. **O debate público** (`debate-publico.md`; seção 16). Os tributos próprios não cobrem a Câmara e a
administração em 2.599 dos 3.356 municípios, onde mora 29,7% da população. A receita por habitante do município
de até 5 mil habitantes é a maior de todas as faixas (R$ 9.647 por morador). Receita por morador não é
dinheiro livre: boa parte é receita externa com destino obrigatório (FUNDEB, SUS), e o que sobra para obra é
outra conta, que o estudo não fez. A Frente Nacional de Prefeitas e Prefeitos (FNP), que se apresenta como
frente de prefeitas e prefeitos de cidades grandes e médias, levantou a pedido da BBC que, em 2023, cerca de
19% dos 5.434 municípios do país com dado tinham 80% ou mais da receita corrente vinda de estados e da União. A
matéria define o indicador; a versão anterior deste texto dizia que a definição não tinha sido localizada, e
estava errada. Com a definição descrita, as contas de 2023 dão 80% nos 13 estados deste estudo; sem a cota do
ICMS e do IPVA, 39% (15.4). A ficha do indicador da FNP não foi localizada. Os dois números medem coisas
diferentes e não dá para dizer quem errou.

14.7. **As saídas** (`solucoes-e-ia.md`; seção 17). Levar a máquina dos 600 municípios de até 5 mil habitantes
ao custo mediano da faixa de 20 a 50 mil do próprio recorte daria R$ 2,35 bilhões por ano. É cenário contábil
de um ano, não previsão: nenhuma fusão foi observada. Equivale a 0,28% da receita municipal das duas regiões, a
11,3% da receita dos 600 municípios e a 64% do que eles gastam com Câmara e administração. Fusão real mediu
menos que isso (15.7). Em São Paulo a conta usa 137 municípios: 138 têm contas utilizáveis e 137 continuam com
até 5 mil habitantes na estimativa de 2024 (Canas passou de 5 mil). A PEC 188/2019 foi arquivada em dezembro de
2022. A LC 230/2026 só trata de desmembrar parte de um município para o vizinho (conferida por artigo jurídico,
não pelo texto oficial).

Os scripts dessas contas estão em `docs/pesquisa/apoio/`. Em 06/10/2026 foram rodados de novo sobre a base
corrigida pela rodada 1: os números batem, com diferença na quarta casa dos expoentes e de R$ 2 na receita por
morador do município grande.

## 15. O que a rodada 2 de revisão e as pesquisas profundas mudaram

Em 06/10/2026 chegaram a auditoria do GPT (33 correções, refeitas uma a uma em
`revisao/claude/r3/CODEX-R2-DIGESTO.md`), a revisão do Grok como leitor hostil do site
(`revisao/grok/RELATORIO-RODADA-2-limpo.md`) e duas pesquisas profundas, do Gemini e do ChatGPT
(`docs/pesquisa/pesquisa-profunda-gemini.md` e `pesquisa-profunda-chatgpt.md`). A conciliação está em
`revisao/claude/CONCILIACAO-RODADA-2.md`. Nenhuma das quatro achou erro de aritmética na base, e as conclusões
de 2024 resistiram. Mudou a classificação em dois pontos, o rótulo e o arredondamento em vários, e o tom em
alguns. A base foi refeita com as duas correções e com 2022 a 2025 dos 13 estados
(`revisao/claude/r3/PIPELINE-RODADA-3.md`).

15.1. **Duas correções de base.**

- *Convênios de capital da saúde.* As contas 2.4.1.4.50 (União, R$ 193,5 milhões em 206 municípios com contas
  utilizáveis) e 2.4.2.2.50 (estado, R$ 242,0 milhões em 342) somam R$ 435,4 milhões e estavam dentro da verba
  negociada restrita, que se diz "sem o SUS". Saíram da restrita e continuam na ampla. O "SUS dentro da medida
  ampla" passou de R$ 3,058 bilhões em 2.142 municípios para R$ 3,493 bilhões em 2.339.
- *Receita corrente e poupança corrente.* As colunas `rec_corrente_liq` e `poupanca_corrente` contavam
  transferência de capital de instituições privadas (R$ 3,346 bilhões em 107 municípios). Foi corrigido. A
  poupança corrente muda mais de 0,5 ponto em 54 municípios e troca de sinal em 7. Nenhum achado usava as duas
  colunas.

Não mudaram: os 3.356 municípios com contas utilizáveis, a receita-base, as oito fatias, a maior fatia, a
dependência, as elasticidades, os testes A, B, C e E, a medida ampla e a emenda sobre a receita. O que mudou
com a primeira correção:

| Número | Publicado | Fica |
|---|---|---|
| Verba estadual restrita, mediana até 20 mil habitantes, São Paulo | 2,54% | 2,45% (2,5% com uma casa, nos dois); Maranhão 0,00% |
| Verba restrita total, mediana até 20 mil habitantes, São Paulo e Maranhão | 3,60% e 1,01% | 3,44% e 0,99% |
| Verba estadual a tamanho igual, São Paulo menos Maranhão (D1e) | +2,3 pontos (2,1 a 2,5) | +2,2 (2,0 a 2,5) |
| Verba federal a tamanho igual (D1u) | -0,9 (-1,3 a -0,5) | -0,9 (-1,3 a -0,5) |
| Entre as regiões, Sudeste menos Nordeste: estadual; federal | +2,1; -1,3 | +2,1 (1,9 a 2,3); -1,2 (-1,4 a -1,0), p = 0,058 depois da correção para vários testes |
| Prefeituras maranhenses de até 20 mil habitantes que lançaram zero de verba estadual restrita | 84 de 127 | 90 de 127 |
| Média da verba estadual restrita, Maranhão e São Paulo | 0,24% e 3,19% | 0,22% e 3,07% |
| Verba negociada restrita sobre o investimento, paulista de até 5 mil habitantes | 53% | 49% (só a estadual: 35%, igual) |
| Triênio São Paulo e Maranhão, verba estadual | 2,1 (1,9 a 2,3) | 2,0 (1,9 a 2,2) |
| Mediana federal na média dos três anos, São Paulo e Maranhão | 0,94% e 1,50% | 0,87% e 1,45% |

A direção de todos os resultados é a mesma. O deck também recebeu a dependência com 8 casas e a receita em
reais de cada município: a contagem por corte, feita depois de arredondar, errava de 1 a 2 municípios em 13
combinações de grupo e corte (o corte de 80% não muda), e o peso da composição por faixa era aproximado.

15.2. **O triênio dos 13 estados.** A pergunta era se 2024, ano de eleição municipal, distorce o retrato fora
de São Paulo e do Maranhão. Não distorce no que o estudo afirma; pesa no investimento, que o estudo usa pouco.
Painel de 3.261 municípios com contas utilizáveis em 2023, 2024 e 2025 (1.594 no Sudeste e 1.667 no Nordeste);
ficam fora 95 dos 3.356 de 2024. Parcelas: média das três parcelas anuais. Valores por habitante: reais de
2025. Diferença a tamanho igual, Sudeste menos Nordeste:

| Comparação | Só 2024 | Média de 2023 a 2025 | Intervalo agrupado por estado, triênio |
|---|---|---|---|
| Dependência, até 50 mil hab. (pontos) | -6,7 (-7,1 a -6,3) | -7,1 (-7,5 a -6,7) | -10,8 a -3,5 |
| Dependência, até 5 mil hab. (pontos) | -3,0 (-3,6 a -2,4) | -3,3 (-3,9 a -2,7) | -5,6 a -1,0 |
| Transferências por hab., até 5 mil | -0,6% (-3,2% a +2,1%) | +0,8% (-1,6% a +3,4%) | -3,4% a +5,3% |
| Transferências por hab., 5 a 50 mil | -5,0% (-6,9% a -3,2%) | -3,5% (-5,3% a -1,7%) | -13,3% a +7,4% |
| Verba federal restrita, até 50 mil (pontos) | -1,24 (-1,44 a -1,03) | -1,22 (-1,40 a -1,05) | -2,44 a -0,01 |
| Verba estadual restrita, até 50 mil (pontos) | +2,08 (1,87 a 2,28) | +2,13 (1,98 a 2,28) | +1,37 a +2,88 |
| Câmara e administração por hab., até 5 mil | -16,9% (-21,7% a -11,9%) | -15,5% (-20,0% a -10,8%) | -29,6% a +1,4% |
| Câmara e administração por hab., 5 a 50 mil | +0,1% (-3,7% a +4,0%) | +0,5% (-3,2% a +4,2%) | -18,7% a +24,2% |
| Investimento por hab., até 50 mil | +34% (27% a 41%) | +42% (36% a 48%) | +13% a +79% |

O intervalo agrupado usa t com 12 graus de liberdade e é o que vale entre regiões.

- *Dependência.* O ano de 2024 dá a menor diferença dos três (7,7 pontos em 2023; 7,0 em 2025). O retrato
  publicado é o lado conservador.
- *Reais por habitante.* Empate entre as regiões, e mais firme: em 2023 o sinal de 5 a 50 mil habitantes era o
  contrário (+1,8%).
- *FPM como maior fatia.* Sudeste 65,0% e Nordeste 46,6% em 2024; 65,1% e 46,8% no triênio. A diferença é de
  18,4 pontos em 2024 (15,1 a 21,7) e 18,3 no triênio (15,0 a 21,6). O que muda é a tendência: 11,6 pontos em
  2023, 19,0 em 2024, 22,2 em 2025, porque no Nordeste o FUNDEB vem passando o FPM. Por estado, 2024 fica a até
  2 pontos do triênio em dez dos treze; fogem Sergipe (62,7% contra 54,7%), Pernambuco (63,4% contra 68,1%) e
  Espírito Santo (44,9% contra 48,7%).
- *Custo da máquina.* Elasticidade de -0,275 em 2024 e -0,278 no triênio; até 5 mil habitantes, -0,908 e
  -0,920.
- *Investimento.* No Nordeste, 2024 é o pico: até 5 mil habitantes, R$ 664 por habitante em 2023, R$ 882 em
  2024 e R$ 761 em 2025; de 10 a 20 mil, R$ 347, R$ 507 e R$ 421. No Sudeste, 2024 repete 2023 e 2025 cai um
  terço (R$ 1.243, R$ 1.292 e R$ 864 até 5 mil habitantes). A vantagem do Sudeste em investimento por habitante
  vai de +87% em 2023 a +34% em 2024 e +13% em 2025. Nenhum achado se apoia nesse número, mas toda razão "sobre
  o investimento" (6.4) herda a oscilação.
- *Sergipe.* A dependência mediana até 20 mil habitantes é 91,3% em 2023, 84,6% em 2024 e 88,7% em 2025. Em
  2024 as demais receitas próprias dos municípios sergipanos saltam de R$ 94 para R$ 584 por habitante. A causa
  provável é a outorga da concessão de saneamento; a fonte não foi aberta.

Ressalva: 2023 e 2025 não passaram pela conferência de 2024 (os alertas de FPM e de FUNDEB só existem para
2024). No Nordeste, as transferências por habitante sobem 17% em termos reais de 2023 para 2024, na mediana até
20 mil habitantes; essa alta não foi conferida em fonte externa.

15.3. **Emenda federal paga em 2025 sobre a receita de 2025, os 13 estados.** Mediana dos municípios de até 20
mil habitantes com contas utilizáveis em 2024, o mesmo recorte de 6.1:

| Estado | Municípios | Sobre a receita de 2025 | Sobre a de 2024 |
|---|---|---|---|
| Sergipe | 51 | 8,5% | 9,3% |
| Piauí | 195 | 7,9% | 9,0% |
| Paraíba | 175 | 7,5% | 8,4% |
| Pernambuco | 85 | 7,2% | 8,0% |
| Rio Grande do Norte | 134 | 6,5% | 7,2% |
| Maranhão | 127 | 5,2% | 5,5% |
| Rio de Janeiro | 22 | 5,1% | 5,8% |
| Espírito Santo | 42 | 5,0% | 5,6% |
| Alagoas | 60 | 4,8% | 5,3% |
| Ceará | 87 | 4,3% | 4,8% |
| Minas Gerais | 656 | 3,5% | 4,0% |
| Bahia | 237 | 3,3% | 3,8% |
| São Paulo | 376 | 1,8% | 2,0% |
| Nordeste | 1.151 | 6,0% | 6,7% |
| Sudeste | 1.096 | 2,9% | 3,2% |

São Paulo segue em último. A parte da tese que fala de verba de deputado federal cai também com os treze
estados e com o denominador do mesmo ano.

15.4. **A conta da FNP refeita.** A matéria da BBC de 30/09/2024 define o indicador: transferências de estados
e da União sobre a receita corrente, em 2023, 5.434 municípios do país. Refeita sobre a série do IPEADATA
(totais da STN, receita bruta) dos 13 estados, no mesmo ano (`revisao/claude/apoio/r3_fnp_definicao.py`):

| Recorte, 2023 | Municípios com dado | 50% ou mais | 80% ou mais | 80% ou mais, sem a cota do ICMS e do IPVA |
|---|---|---|---|---|
| 13 estados | 3.452 | 99,1% | 80,4% | 38,8% |
| Sudeste | 1.665 | 98,4% | 66,8% | 11,1% |
| Nordeste | 1.787 | 99,8% | 93,0% | 64,6% |
| São Paulo | 645 | 96,3% | 52,4% | 0,3% |
| Maranhão | 217 | 100,0% | 96,3% | 82,5% |

O número de "50% ou mais" da FNP (94,8% no país) é compatível com este (99,1% nas duas regiões). O de "80% ou
mais" não se reproduz com a definição descrita: só os 2.774 municípios do Nordeste e do Sudeste acima de 80% já
seriam 51% dos 5.434 da conta da FNP, contra "cerca de 19%". A ficha do indicador no anuário da FNP não foi
localizada. O que se pode dizer é que os dois números medem coisas diferentes e que a definição escrita na
matéria não leva aos 19%. A hipótese de que a FNP contaria só verba da União foi descartada pelo texto da
matéria, que diz "Estados ou União".

15.5. **A pizza média.** Parcela média de cada fonte na receita, média simples dos municípios com contas
utilizáveis em 2024 (`docs/tabelas/pizza_media_por_grupo_2024.csv`):

| Fonte | Sudeste | Nordeste | São Paulo | Maranhão |
|---|---|---|---|---|
| FPM | 29,7% | 29,6% | 26,3% | 23,5% |
| FUNDEB | 12,3% | 28,6% | 12,7% | 39,5% |
| Cota do ICMS e do IPVA | 17,7% | 9,2% | 21,6% | 7,9% |
| SUS | 10,1% | 12,4% | 7,2% | 12,6% |
| Royalties | 2,7% | 1,0% | 1,1% | 1,1% |
| Outras transferências | 10,5% | 10,1% | 9,3% | 8,3% |
| **Receita externa (soma das seis)** | **83,1%** | **90,8%** | **78,2%** | **93,1%** |
| Tributos próprios | 12,6% | 6,6% | 16,9% | 5,2% |
| Demais receitas próprias | 4,4% | 2,6% | 4,9% | 1,7% |
| **Receita interna (soma das duas)** | **16,9%** | **9,2%** | **21,8%** | **6,9%** |
| Receita externa, só até 5 mil habitantes | 91,0% | 93,9% | 89,5% | 95,5% (5 municípios) |

No município médio a receita externa é 83% no Sudeste e 91% no Nordeste, com desvio-padrão de 11 e de 7
pontos. O FPM pesa o mesmo nas duas regiões (30% e 30%). A diferença está no FUNDEB (12% no Sudeste e 29% no
Nordeste), na cota do ICMS e do IPVA (18% e 9%) e nos tributos próprios (13% e 7%). Até 5 mil habitantes as
duas regiões quase se encontram: 91% e 94%. É média de parcelas, cada município com o mesmo peso; na soma em
reais o Sudeste tem 58% de receita externa e o Nordeste 80%, porque o imposto próprio se concentra nas cidades
grandes.

15.6. **Território.** Os municípios de até 50 mil habitantes administram 81,5% da área dos 13 estados, com
30,1% da população; os de até 20 mil, 50,4% da área e 14,9% da população
(`docs/tabelas/territorio_por_tamanho_2022.csv`, Censo 2022):

| Municípios de até 50 mil habitantes | Municípios | Parcela da área | Parcela da população |
|---|---|---|---|
| Sudeste | 1.411 (84,6%) | 79,1% | 20,8% |
| Nordeste | 1.619 (90,2%) | 82,9% | 44,5% |
| São Paulo | 508 (78,8%) | 74,9% | 15,1% |
| Maranhão | 195 (89,9%) | 78,6% | 51,7% |
| 13 estados | 3.030 (87,5%) | 81,5% | 30,1% |

O dado descreve quem administra o território. Não mede demanda nem custo de servir área grande com pouca gente.

15.7. **Leituras novas.** Das pesquisas profundas só entrou o que foi aberto na fonte; a marca está ao lado.

- *Reforma tributária* (Gobetti e Monteiro, IPEA, 2023, tabela 2 e tabela A.1; conferido na fonte). No cenário
  estático da nota, 480 dos 645 municípios paulistas ganham e 165 perdem; no Maranhão, 204 de 217 ganham.
  Sandovalina, na região de Presidente Prudente, está na lista de 32 cidades com risco de queda, que são em
  geral sedes de refinaria ou de hidrelétrica. A simulação usou 85% por população. A regra aprovada reparte a
  cota municipal do IBS assim: 80% por população, 10% por educação, 5% por preservação ambiental e 5% em partes
  iguais (Constituição, art. 158, § 2º).
- *Emancipações* (LC 651/1990 de São Paulo, art. 2º, conferida na ALESP; Tomio, 2002, p. 78 e 79; Brandt, 2010,
  p. 63 e 64). São Paulo exigia 1.000 eleitores, e o Maranhão também. O piso legal não explica por que os novos
  municípios maranhenses nasceram maiores. A pergunta segue aberta.
- *O que fusões reais mediram.* Israel: queda de cerca de 9% do gasto dos municípios fundidos (Reingewertz,
  2012; resumo). Brandemburgo: 8% a 10% do gasto administrativo em média, cerca de 20% na fusão compulsória e
  zero na voluntária (Blesse e Baskaran, 2016; texto para discussão). Dinamarca e Holanda: efeito nulo no gasto
  total (Blom-Hansen e coautores, 2016, resumo; Allers e Geertsema, 2016). O cenário de 14.7 equivale a 11,3%
  da receita dos 600 municípios e a 64% do gasto deles com a máquina: fica acima do que fusão real mediu.
- *Degraus do FPM* (Corbi, Papaioannou e Surico, 2019; Litschig, 2012; conferidos). Ver 10.5.
- *Imposto próprio contra transferência* (Gadenne, 2017; só a referência e o resumo). Em municípios brasileiros,
  receita de imposto próprio a mais vira escola; transferência a mais, com a mesma liberdade de uso, não muda a
  infraestrutura. Se valer aqui, muda a leitura de "depender": importa de onde vem o dinheiro e também como ele
  é gasto. É leitura a fazer, não resultado do estudo.

## O que ainda não se sabe

Saiu desta lista o que a rodada 2 respondeu: se 2024, ano de eleição, distorce o retrato nos outros onze
estados (não distorce no que o estudo afirma; 15.2); a emenda de 2025 sobre a receita de 2025 em Minas, no
Espírito Santo e no Rio (15.3); o exemplo de Sandovalina na reforma tributária (conferido; 15.7); e a
definição do indicador da FNP, que está na matéria (15.4). O que segue aberto:

1. Qual é a ficha do indicador da FNP, a dos 19%.
2. Por que os municípios criados no Maranhão de 1988 a 2000 nasceram maiores, se o piso legal era o mesmo de
   São Paulo.
3. Emenda e convênio estaduais por município e por programa. Os PDFs de emendas impositivas da ALESP (2019 a
   2026, só o valor aprovado) e os convênios de saída de Minas (CSV diário da Controladoria-Geral do Estado) já
   foram localizados; falta extrair e casar com a execução. A extensão da rastreabilidade às emendas estaduais
   pelo STF (ADPF 854) veio de resumo de busca e não foi conferida.
4. Se o governo do Maranhão investe direto nos municípios, sem passar pela conta da prefeitura (6.3).
5. A prévia do Censo de dezembro de 2022 contra o resultado final, nos degraus do FPM (10.4). O diretório está
   no FTP do IBGE; o arquivo por município é datado de 22/06/2023 e falta ver qual é a data de corte.
6. Uma medida de necessidade de gasto por município, para testar "recebe mais do que deveria" nos dois
   sentidos (4.5).
7. Quantos dos 150 municípios pequenos paulistas estão em arranjo populacional: cruzar a base com a REGIC 2018.
8. Se a emenda por habitante resiste ao controle por partido do prefeito e margem da eleição. Baião e Couto
   (2017) mostram, no resumo, que mais emenda é proposta e executada nas prefeituras do partido do deputado; o
   estudo não tem essa variável.
9. Quanto de renda local o município pequeno perderia num FPM proporcional, com multiplicador perto de 2
   (10.5).
10. Se imposto próprio rende mais serviço que transferência (Gadenne, 2017; 15.7).
11. A série de emendas pelo ano do pagamento, por tipo, e por beneficiário final (14.4).
12. Os planos de contas de antes de 2022, para um painel conta a conta desde 2013. Os dados de 2019 a 2021 dos
    13 estados já estão em disco. A conta 1.7.1.8.04 é assistência social em 2018 e SUS de 2019 a 2021 (achado
    do GPT), então cada plano antigo precisa de regra própria.

Seguem abertos de antes, fora da lista da conciliação:

- Quanto da cota do ICMS de cada município é devolução (valor adicionado) e quanto é rateio.
- O custo da máquina numa medida que valha para todos os estados.
- Quanto pesa cada causa da concentração de municípios acima dos degraus do FPM (10.4).
- O efeito da reforma tributária município a município. A nota do IPEA só traz tabela por estado e a lista de
  32 cidades; a simulação usou 85% por população, e a regra aprovada usa 80%. A transição só foi vista em
  resumo de busca.
- Se a alta real de 17% das transferências por habitante no Nordeste de 2023 para 2024 é dado ou é declaração:
  2023 e 2025 não passaram pela conferência de 2024. E a causa do salto de receita própria em Sergipe em 2024.
- Se os 40 municípios que lançaram ITR como imposto próprio têm convênio com a Receita Federal, e a declaração
  dos 18 que lançaram ICMS ou IPI como imposto.

## Conferência

### Conferência interna

Oito agentes independentes tentaram derrubar esta análise em 05/10/2026; os relatórios estão em
`revisao/claude/`. O que se confirmou: a réplica independente da receita bate com a base nos municípios todos;
a despesa bate com o dado bruto ao centavo; cerca de 150 números do texto foram refeitos; seis testes refeitos
batem até a quinta casa; a série longa é idêntica à DCA em 2024. O que eles derrubaram e foi corrigido:

| O que estava escrito | O que o dado sustenta |
|---|---|
| "A tamanho igual, o maranhense recebe 9% a mais por habitante" | Vale de 5 mil habitantes para cima; abaixo disso não dá para dizer (4.1) |
| "O nordestino recebe 2,5% a mais que o do Sudeste" | Não se distingue de zero; dependia de Minas (4.1) |
| "Convênio pesa mais em São Paulo" | Só o convênio estadual; o federal pesa mais no Maranhão (6.3) |
| "Nas estimativas o excesso acima dos degraus some" | Ele se desloca para 2% a 5% acima (10.3) |
| "A dependência caiu devagar desde 2000" | Parada de 2002 a 2021; a queda de 2000 a 2002 é troca de classificação (11.1, 11.2) |
| "O FPM trocou de endereço" | Convergiu; o Sudeste só passou à frente em 2023 e 2024, por Minas (11.3) |
| "Elasticidade de -0,28 no custo da máquina" | De -0,91 no município minúsculo a zero acima de 20 mil habitantes (7.2) |
| "Sem diferença de custo entre Sudeste e Nordeste" | Sem diferença estável, e a medida não é comparável entre estados (7.3) |
| "86% dos paulistas minúsculos são doadores do FUNDEB" | 93%, depois de tirar 17 prefeituras com a dedução declarada errado (8.1) |
| "O FUNDEB tira do paulista e põe no maranhense" | São fundos estaduais separados (8.2) |
| "CAPAG C em 62% e 62%" | 63% e 63% entre os que têm nota; no topo SP está melhor (9.1) |

### Revisão cruzada (rodada 1, 05/10/2026)

O GPT auditou e replicou as contas (`revisao/gpt/`); o Grok fez o contraditório e a checagem de fatos
(`revisao/grok/`). A conciliação está em `revisao/claude/CONCILIACAO-RODADA-1.md` e o que foi aplicado, em
`revisao/claude/APLICADO-RODADA-1.md`. Nenhum dos dois derrubou a aritmética: a réplica cega do GPT bate em 150
municípios. O que mudou:

| O que estava escrito | O que ficou |
|---|---|
| "Fica de pé pela contagem de municípios" | Depende do corte: 338 contra 210 acima de 80%; 92 contra 184 acima de 90% (Resposta curta, 1.3, 13) |
| "Transferências voluntárias" de 4,2% da receita no paulista pequeno | A medida tinha R$ 3,493 bilhões do SUS. Na restrita, 2,5%; o nome passou a "convênios e transferências de capital" (6) |
| "Três quartos do investimento" | 49% na medida restrita; 74% na ampla (6.4) |
| "O Maranhão recebe 0,0% do estado" | É mediana de lançamento: 90 de 127 lançaram zero; média de 0,22% (6.3) |
| "Cerca de 12% a menos por habitante" | De 9% a 12%, conforme o recorte e os anos; o 12% é de teste escrito depois de ver o dado (4.1) |
| "Empatam" até 5 mil habitantes | Vale para as regiões; para SP contra MA não dá para dizer (4.1) |
| "Emenda: 2,0% e 5,5% da receita" | Era emenda de 2025 sobre receita de 2024. Sobre a de 2025: 1,8% e 5,2% (6.1) |
| "Logo acima de cada degrau" | A soma dos degraus tem excesso; degrau a degrau, quatro dos dezessete (10.2) |
| "Não mostra a causa" | Há causas documentadas; falta medir o peso de cada uma (10.4) |
| "Provavelmente rendimento de aplicação" | A conta de rendimento explica a queda em São Paulo e menos da metade no Maranhão (11.1) |
| FPM "voltou" em São Paulo | Parte é a EC 112/2021, cerca de 3% a mais de 2022 a 2025 (11.3, 11.7) |
| "O interior profundo tem endereço: o oeste" | O oeste é onde estão os municípios pequenos; a tamanho igual não se separa (12.2) |
| "A reforma tira receita do município pequeno" | Do pequeno com usina ou indústria; o pequeno sem valor adicionado tende a ganhar |
| ICMS e IPI lançados como imposto próprio (18 municípios) | Passaram a cota de ICMS e de IPI; Salto/SP mudou de maior fatia (2, tabela) |
| "Critério da PEC 188" | Simulação, na leitura da CNM; PEC arquivada em 22/12/2022 (7.5) |

Saíram da análise 106 municípios: 93 com dedução do FUNDEB fora da faixa de 10% a 25% da cesta (17 em São
Paulo, 25 na Bahia, 19 na Paraíba, 11 em Minas), 1 sem cesta declarada (Bandeira do Sul/MG), 8 que não
entregaram as contas, 3 com receita nula ou negativa e 1 com conta visivelmente incompleta. Outros 100 com
contas utilizáveis têm alerta de FPM ou de FUNDEB e continuam dentro; tirá-los não muda A1 nem C1 (família S).

Achado a achado. "Confirma" quer dizer que o revisor refez a conta ou abriu a fonte. A nota do Grok é a
confiança dele de 0 a 10; quando há duas, a primeira é do número e a segunda da leitura.

| Achado | Conferência interna | GPT | Grok |
|---|---|---|---|
| 1. Quantos são pequenos | feita | não olhou a tabela; contestou "fica de pé pela contagem" | confirma, nota 9 |
| 2. Maior fatia | feita | confirma, também no triênio; contestou o rótulo da fatia SUS | confirma a conta (8); contestou a frase de abertura (5), pela inversão em 2.3 |
| 3. Parcela da receita | feita | confirma, também no triênio; contestou o perímetro (saúde dos servidores, ICMS e IPI em imposto), já corrigido | confirma a direção (8); contestou a frase (6): SP contra MA é exploratório |
| 4. Reais por habitante | feita | confirma de 5 a 50 mil; contestou "empate" para SP contra MA | confirma com ressalva (7): o 12% é de teste pós-verificação |
| 5. Por município ou por morador | feita | confirma | confirma, nota 9; pediu o denominador |
| 6.1 e 6.2. Emenda federal | feita | contestou o denominador de 2024; não fez média de três anos | número (7), leitura (4): o pago mistura restos a pagar |
| 6.3 a 6.6. Convênio | feita | contestou: SUS dentro da medida | mediana (6); contestou "o estado do MA não manda nada" (3) |
| 7.1 a 7.4. Máquina | feita | só conferiu que a soma das funções fecha; não refez elasticidades | dentro de SP (7), entre estados (3) |
| 7.5. PEC 188 | feita | não olhou | simulação (6), regra vigente (2): PEC arquivada |
| 8. FUNDEB | feita | confirma as 94 exclusões; apontou 62 suspeitos, que não mudam o resultado | percentual (6), livre contra carimbado (7) |
| 9. Saúde fiscal | feita | não olhou | percentuais (8); contestou "igualmente saudáveis" (4) |
| 10. Degraus do FPM | feita | confirma com teste de densidade; contestou "cada degrau" | contagem (8), causa (3); trouxe as liminares |
| 11. Evolução | feita | confirma 11.7 e a conta de 11.1, não a causa; não refez 11.2 a 11.6 | nota 6; trouxe a EC 112/2021 |
| 12. Interior paulista por região | feita | não olhou | tabela (8); contestou "efeito do oeste" (4), com razão (12.2) |
| 13. Dependência como classe única | seção nova, feita nesta rodada | a ideia é dele; números refeitos e iguais | não olhou |

Os números das duas tabelas acima que dependem da medida restrita já são os da base refeita na rodada 2
(49%, 90 de 127, 0,22%, R$ 3,493 bilhões); a rodada 1 tinha deixado 53%, 84 de 127, 0,24% e R$ 3,058 bilhões.

### Revisão cruzada (rodada 2, 06/10/2026)

O GPT, no Codex, auditou de novo a base, o relatório e o deck publicados. O Grok leu o site como leitor hostil
e como leitor leigo, e conferiu fatos. Duas pesquisas profundas, do Gemini e do ChatGPT, procuraram literatura
e contradições. Tudo foi refeito ou aberto na fonte antes de entrar (`revisao/claude/r3/CODEX-R2-DIGESTO.md`,
`docs/pesquisa/pesquisa-profunda-*.md`, `docs/pesquisa/fatos-rodada-3.md`). A conciliação está em
`revisao/claude/CONCILIACAO-RODADA-2.md`.

**O que o GPT confirmou**, em réplica independente, sem importar o código do projeto:

- o universo: 3.462 municípios, 3.356 com contas utilizáveis, 106 fora, com o crivo reconstruído sem
  divergência; a receita de 2024 refeita das folhas brutas, com a base e as oito fatias fechando;
- a dependência a tamanho igual: 13,5 pontos a mais no Maranhão e 6,7 no Nordeste; com PIB por habitante, 10,3
  e 3,2;
- os cortes: 338 de 628 em São Paulo e 210 de 215 no Maranhão acima de 80%; 92 e 184 acima de 90%; os 72
  percentuais das tabelas da seção 13;
- a receita externa sobre a soma da receita, 49% e 87%; as transferências por habitante até 5 mil habitantes,
  R$ 8.859 e R$ 8.457;
- as elasticidades da máquina (-0,908; -0,404; -0,067) e as 374 linhas de expoentes da seção 14.2;
- a emenda por habitante, R$ 149 e R$ 357, e sobre a receita de 2025, 1,8% e 5,2%;
- a série de 2002 a 2025 (89,1% para 86,3% em São Paulo; 97,7% para 94,7% no Maranhão);
- o oeste paulista: 0,9 ponto, intervalo de -0,2 a +2,0;
- os índices de representação (10,4% na Câmara; 11,8% no Congresso; 8,4% redistribuída) e as cadeiras por
  estado, iguais às da página da Câmara;
- a aritmética da série de emendas e o cenário de R$ 2,35 bilhões, com as 20 células da tabela;
- o deck: 54 slides sem texto cortado e os dados servidos sem divergência com a base.

Refeitos também por mim, e iguais: o universo, o corte de 80%, os R$ 149 e R$ 357, os 1,8% e 5,2%, os
R$ 8.859, os três índices de representação, o cenário de fusão, o contrafactual do FPM e os testes D1.

**O que o GPT pediu** (33 correções, todas confirmadas ou registradas como pista):

| Pedido | O que ficou |
|---|---|
| Tirar da medida restrita os convênios de capital da saúde | Feito (15.1): +2,3 vira +2,2 pontos; 53% vira 49% |
| Tirar o capital privado da receita corrente e da poupança corrente | Feito (15.1); nenhum achado usava |
| Dizer que a série de emendas é por orçamento, não por ano de pagamento | Feito no texto (14.4); a série pelo ano do pagamento por tipo fica para depois |
| Contar os municípios por corte sem arredondar antes; pesar a composição pela receita em reais | Feito no deck (15.1) |
| Denominador da população acima de 80% | Feito: sobre toda a população, 7,1%, 78,5%, 16,5% e 56,5% (seção 5) |
| Dez arredondamentos de último algarismo | Os oito que tocam este arquivo: CAPAG 25,1% e 9,6%; Bahia R$ 233; Senado 37,3%; emenda 6,5 vezes; tributo próprio 3,6%; R$ 3,5 mil; R$ 5.925 e R$ 3.194; -3,1%. Os outros dois são do relatório (emenda sobre a receita de 2024 na faixa de 10 a 20 mil, 1,7% e 5,1%; inclinações do contrafactual do FPM) |
| "137 declararam a despesa por função" e "mediana da sua região" | Corrigidos (14.7): 137 continuam com até 5 mil habitantes na estimativa de 2024; mediana do próprio recorte |
| R$ 2,35 bilhões como cenário, não como teto demonstrado | Feito (14.7) |
| "Receita total" na resposta à nota do CEM | Vira "receita-base" (14.5) |
| Universo da simulação da PEC 188 | Declarado (7.5): 616 no total, 594 entre as utilizáveis |
| "Só se igualam em zero"; "0,1 ponto acima" | Reescritos (13.1 e 13.3), com a conta dele, não refeita |
| O expoente 0,83 de Bettencourt ao lado da máquina municipal | No deck e no relatório vira analogia do autor ou sai; não estava neste arquivo |
| Fixar a contagem de arquivos e o tamanho do dado bruto com data | Vai para o método do deck e do relatório |

**O que o Grok pediu**, como leitor hostil: tirar o carimbo "Cai" de cima dos 13,5 pontos, que são conta
exploratória (o teste registrado antes é o regional, de 6,7); pôr as definições antes das respostas; dizer o
que entra na receita externa ao lado da classe de 80%, porque FUNDEB e SUS têm destino obrigatório; pôr "90 de
127 lançaram zero" junto do 0,0% do Maranhão; trocar "há município demais" por "há mais municípios logo acima
do degrau do que logo abaixo"; apagar "não bate" e "não cabem juntos" da comparação com a FNP, porque a
matéria define o indicador; reescrever a resposta a Ricardo Amorim como outra grandeza; tirar os percentuais
tirados de 62 comentários de vídeo; tirar o destaque dos R$ 2,35 bilhões; corrigir a data da reportagem do
orçamento secreto e incluir os marcos de agosto de 2024 no STF; e trazer as vozes que faltavam (prefeito de
município pequeno, parlamentar que defende emenda, gente do Nordeste, Marcos Mendes). Tudo isso foi aceito. A
maior parte é texto do deck e do relatório; neste arquivo mudaram 5.1, 6.3, 10, 14.5, 14.6 e 14.7.

**O que não foi aceito.**

- Das pesquisas profundas: nenhum número ou referência que a conferência marcou como errado ou não encontrado.
  Exemplos: Caselli e Michaels (2013) apresentado como estudo de fusão (é sobre royalties de petróleo); o piso
  de 4 a 5 mil habitantes para emancipação no Maranhão (as fontes dão 1.000 eleitores); a economia de 15% a
  30% com consórcios (o artigo citado não mede economia); o multiplicador de 0,6 a 0,8 para o FPM (o artigo
  diz perto de 2). Nenhuma das contradições que elas apontaram derrubou achado.
- Do Grok: cortar o bloco de inteligência artificial do deck. Fica, mais curto, por ser pedido do dono.
- Do dono: chamar o vídeo de 2019 da Gazeta do Povo de anti-bolsonarista e afirmar fim eleitoral na PEC 188.
  As fontes descrevem o jornal, naquele período, como de direita e favorável às reformas do Ministério da
  Economia, e não foi localizado registro de motivação eleitoral ou regional. O que se sustenta: o verbo dos
  títulos assusta e não é o do texto, e isso valeu para a imprensa em geral, inclusive a agência oficial.
- A série de emendas pelo ano do pagamento por tipo: fica para depois; nesta versão muda o rótulo.
