# Achados

Retrato das contas de 2024 dos municípios do Nordeste e do Sudeste (3.356 com contas utilizáveis, de 3.462) e
evolução de 2002 a 2025. Todo número daqui sai de `docs/NUMEROS.md`, `docs/TESTES.md`, `docs/tabelas/` ou de
`revisao/claude/apoio/r1_numeros_extras.txt`. O método está em `docs/METODO.md`. Versão de 06/10/2026, corrigida
pela conferência interna (`revisao/claude/`) e pela revisão cruzada do GPT e do Grok
(`revisao/claude/CONCILIACAO-RODADA-1.md`); o que cada uma mudou está no fim.

## Resposta curta

A tese "o interior profundo de São Paulo depende de verba externa e de deputado tanto quanto, ou mais que, o
Maranhão" tem uma parte que vale em número de prefeituras, uma que empata e duas que caem.

- **Vale em número de prefeituras, e depende do corte.** São Paulo tem 150 municípios de até 5 mil habitantes;
  o Maranhão tem 5. Nos paulistas, 90% da receita vem de transferência e cada morador recebe em torno de
  R$ 9,2 mil por ano de fora, 72% a mais que no município maranhense típico (R$ 5,4 mil). Acima de 80% de
  dependência há mais prefeituras em São Paulo (338 contra 210). Acima de 90%, o Maranhão tem o dobro (184
  contra 92). Em proporção dos municípios, o Maranhão fica acima em todo corte de 50% a 95% (seção 13). O FPM
  é a maior fonte em 53% dos municípios paulistas e em 7% dos maranhenses; com o FUNDEB contado pelo saldo, em
  55% e 35%.
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

2.1. São Paulo fica em mosaico: FPM no oeste e no Vale do Ribeira, ICMS onde há usina, indústria ou refinaria,
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

2.6. A fatia "SUS" é só o repasse fundo a fundo corrente. O SUS de convênio e de capital (R$ 3,058 bilhões em
2.142 municípios) fica em "outras transferências" (`docs/METODO.md`).

2.7. Na média de 2023 a 2025, no painel de 830 municípios de São Paulo e do Maranhão com contas utilizáveis
nos três anos, o resultado é o mesmo: FPM em 52,2% dos paulistas, FUNDEB em 90,1% dos maranhenses.

Figuras: `05_mapa_maior_fatia_SP_MA`, `05_mapa_maior_fatia_sensibilidade_SP_MA`, `11_mapa_maior_fatia_SE_NE`,
`12_placar_maior_fatia_por_uf`, `04_composicao_receita_*`.

## 3. Dependência em parcela da receita

Mediana da parcela da receita que vem de transferências:

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

3.3. Tributo próprio: na mediana, 7,4% da receita no paulista de até 5 mil habitantes e 3,7% no nordestino.
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
  -3,0% com intervalo de -18% a +15% em 2024, e de -1,5% (-17% a +16%) na média de 2023 a 2025. A mediana dos
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
| Média dos municípios | R$ 5.924 | R$ 5.642 |
| Mediana dos municípios | R$ 5.123 | R$ 5.375 |
| Por morador (soma sobre soma) | R$ 3.193 | R$ 4.527 |

Na média por município São Paulo recebe mais, porque tem muito município minúsculo; na mediana e por morador,
recebe menos. O município do Sudeste de até 5 mil habitantes recebe cerca de R$ 3,4 mil a mais por habitante
que o nordestino de 10 a 20 mil, que é o tamanho mais comum lá (teste B3).

4.3. O que cai com o tamanho é forte: o FPM líquido por habitante vai de R$ 4.137 (paulista de até 5 mil) a
R$ 1.177 (20 a 50 mil). Borá, com 907 habitantes no Censo, recebeu R$ 17,5 milhões de FPM bruto em 2024.

4.4. A cota mínima do FPM vale 10% a mais em São Paulo que no Maranhão, porque a fatia de cada estado está
congelada desde 1990 (`docs/pesquisa/fpm.md`).

Figuras: `06_dependencia_*`, `14_transferencias_por_habitante_por_uf`.

## 5. Por município ou por morador

| Municípios com mais de 80% da receita vinda de transferências | SP | MA | Sudeste | Nordeste |
|---|---|---|---|---|
| Parcela dos municípios com contas utilizáveis | 53,8% | 97,7% | 70,1% | 93,2% |
| Parcela da população que mora neles | 7,1% | 78,7% | 16,6% | 57,8% |

5.1. É aqui que mora o mal-entendido. São 53,8% das 628 prefeituras paulistas com contas utilizáveis (338) e
97,7% das 215 maranhenses (210). Nas paulistas mora um paulista em cada catorze. No Maranhão, quase quatro em
cada cinco moradores. Somando tudo, as transferências são 49% da receita dos municípios paulistas e 87% da dos
maranhenses.

5.2. Contando todos os municípios, e supondo os de contas não utilizáveis todos abaixo ou todos acima do
corte, a parcela fica entre 52,4% e 55,0% dos 645 paulistas e entre 96,8% e 97,7% dos 217 maranhenses.

## 6. Verba negociada: emenda e convênio

Esta seção mudou na revisão cruzada. O que o estudo chamava de "transferências voluntárias" tinha R$ 3,058
bilhões do SUS dentro, e a Lei de Responsabilidade Fiscal (art. 25) tira o SUS dessa categoria. A medida
principal passou a ser a restrita: convênios e transferências de capital, sem o SUS e sem o convênio corrente
estadual de educação, que pode ser repasse regular. A medida ampla, a de antes, fica como sensibilidade.
Nenhuma das duas é a "transferência voluntária" da lei (`docs/METODO.md`).

6.1. **Emenda federal.** Pagas em 2025 a prefeituras e fundos municipais (Portal da Transparência; o valor pago
inclui restos a pagar de anos anteriores), por habitante, mediana dos municípios de até 20 mil habitantes:
Sergipe R$ 670, Piauí R$ 622, Paraíba R$ 586, Rio de Janeiro R$ 518, Rio Grande do Norte R$ 493, Pernambuco
R$ 462, Alagoas R$ 454, Espírito Santo R$ 378, Maranhão R$ 357, Ceará R$ 294, Minas R$ 274, Bahia R$ 234, São
Paulo R$ 149. São Paulo é o último na mediana, na média e ponderando por população. Em parcela da receita de
2025: 1,8% em São Paulo, 5,2% no Maranhão, 7,9% no Piauí. Sobre a receita de 2024, que era o denominador da
versão anterior: 2,0%, 5,5% e 9,0%. A base de 2025 ainda não existe para Minas, Espírito Santo e Rio.

6.2. A tamanho igual, o Maranhão recebe R$ 240 a mais de emenda federal por habitante que São Paulo, e o
Nordeste R$ 235 a mais que o Sudeste (teste D3). É o que a regra produz: a cota é por parlamentar e por
bancada, e São Paulo tem um deputado federal para cada 634 mil habitantes; o Maranhão, um para cada 376 mil. O
arquivo só cobre prefeitura e fundo municipal; em São Paulo, um terço da emenda com destino no estado vai para
o governo estadual e para entidades, e isso fica fora.

6.3. **Convênio e transferência de capital nas contas da prefeitura**, medida restrita, mediana dos municípios
de até 20 mil habitantes, em parcela da receita:

| De quem vem | SP | MA | Outros |
|---|---|---|---|
| União, restrita | 0,66% | 0,75% | Piauí 3,3%, Paraíba 3,9% |
| União, ampla | 0,74% | 0,90% | Piauí 3,9%, Paraíba 4,3% |
| Estado, restrita | 2,5% | 0,0% | Espírito Santo 6,0%, Minas 2,3%, Rio 0,0% |
| Estado, ampla | 4,2% | 0,0% | Espírito Santo 6,4%, Minas 3,3%, Rio 0,0% |

A tamanho igual, na medida restrita, o paulista tem 2,3 pontos a mais de verba estadual (2,1 a 2,5) e 0,9
ponto a menos de verba federal (0,5 a 1,3) que o maranhense (testes D1e e D1u). Na ampla, 4,4 pontos a mais e
1,0 a menos. Entre as regiões, o Sudeste tem 2,1 pontos a mais de verba estadual na restrita; a diferença
federal (1,3 ponto a favor do Nordeste) não se distingue de zero com erro agrupado por estado.

O 0,0% do Maranhão é mediana de lançamento, não prova de que o estado não repassa. Das 127 prefeituras
maranhenses de até 20 mil habitantes, 84 lançaram zero nessas contas (68 na medida ampla). Na média, a verba
estadual é 0,24% da receita no Maranhão e 3,19% em São Paulo (0,36% e 5,22% na ampla).

6.4. O que São Paulo tem de diferente é o governo do estado como fonte de verba negociada, e o tamanho disso
caiu com a medida restrita: de 4,2% para 2,5% da receita. No município paulista de até 5 mil habitantes, a
verba negociada (federal e estadual) equivale a 53% do investimento, e só a estadual a 35%. Na medida ampla
eram 74% e 56%.

6.5. Essa medida não enxerga a emenda. Seis em cada dez reais de emenda vão para o fundo municipal de saúde e
entram na conta do SUS; e a conta própria da emenda Pix registra 69% do valor pago em São Paulo e 24% no
Maranhão, onde o dinheiro aparece em "outras transferências da União". Para emenda, vale só o Portal.

6.6. O que falta medir: emenda de deputado estadual e convênio estadual por município e por programa. É a peça
que decide a versão "verba de deputado" da tese.

6.7. Na média de 2023 a 2025 (São Paulo e Maranhão, 671 municípios de até 50 mil habitantes) o resultado se
mantém: 2,1 pontos a mais de verba estadual em São Paulo (1,9 a 2,3) e 1,0 ponto a menos de verba federal (0,7
a 1,3), na medida restrita. O ano de 2024 foi fraco de convênio federal: a mediana dos municípios de até 20
mil habitantes, 0,66% em São Paulo e 0,75% no Maranhão em 2024, é de 0,94% e 1,50% na média dos três anos.

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

7.5. Simulação do critério de extinção da PEC 188/2019 (menos de 5 mil habitantes e IPTU, ITBI e ISS abaixo de
10% da receita), na leitura da CNM, que usou a receita corrente líquida como denominador, sobre as contas de
2024: 242 municípios em Minas, 133 em São Paulo, 83 no Piauí, 68 na Paraíba, 49 no Rio Grande do Norte e 5 no
Maranhão. Fica perto da lista da CNM de 2019 (223, 135, 75, 68, 48 e 4). A PEC foi arquivada em 22/12/2022; não
há proposta em tramitação com esse critério. O texto do critério na PEC protocolada não foi aberto por
ninguém nesta revisão.

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
| A ou A+ | 22,0% | 14,3% | 25,0% | 9,7% |
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
o coeficiente efetivo. Para este estudo, o recado é que perto dos degraus a população não é uma medida neutra
do tamanho.

## 11. Evolução de 2002 a 2025

Série do IPEADATA, receita bruta, que tem os mesmos totais das contas anuais. A "dependência" desta série é
transferência corrente sobre receita corrente bruta. Não é a mesma variável da seção 3, que é líquida das
deduções e sem a previdência própria; os níveis não se comparam. Municípios de até 20 mil habitantes, mediana
dos que aparecem nos dois anos (teste G):

| | 2002 | 2025 | Mudança (pontos) |
|---|---|---|---|
| Transferências correntes sobre a receita corrente, SP | 89,1% | 86,3% | -2,7 |
| Idem, MA | 97,8% | 94,5% | -3,2 |
| Idem, Sudeste | 92,3% | 88,7% | -3,1 |
| Idem, Nordeste | 96,7% | 93,0% | -3,4 |
| FPM sobre a receita corrente, SP | 37,3% | 35,5% | -1,6 |
| Idem, MA | 52,8% | 28,9% | -23,2 |
| Idem, Sudeste | 49,7% | 40,9% | -6,5 |
| Idem, Nordeste | 52,6% | 36,3% | -16,1 |
| Cota-parte do ICMS sobre a receita corrente, SP | 26,2% | 20,9% | -5,4 |
| Idem, MA | 4,7% | 9,6% | +4,9 |
| Câmara e administração sobre a receita corrente, SP | 18,3% | 13,1% | -4,6 |
| Idem, MA | 21,0% | 14,7% | -6,7 |

11.1. A dependência quase não se mexeu. De 2002 a 2021 a mediana caiu menos de um ponto; os outros dois ou três
vieram depois de 2021, e a maior parte não é imposto próprio. Segundo a conta do GPT (não refeita por mim: a
série longa não traz essa conta), de 2021 para 2022, nos municípios de até 10 mil habitantes, a dependência
caiu 1,4 ponto nos dois estados e o rendimento financeiro subiu 1,4 ponto da receita em São Paulo e 0,6 no
Maranhão. A conta de rendimento explica a queda em São Paulo e menos da metade no Maranhão. Que a causa seja o
juro alto segue hipótese. A distância entre São Paulo e o Maranhão é a mesma de 2002 (cerca de 8 pontos).

11.2. A série começa em 2002 de propósito. Até 2001 o imposto de renda retido na fonte entrava como
transferência e a função Administração tinha outra classificação; comparar com 2000 fabrica queda.

11.3. O peso do FPM caiu muito mais no Nordeste (16 pontos) que no Sudeste (6,5), e no Maranhão caiu quase à
metade, com o FUNDEB e o ICMS ocupando o lugar: é troca de uma transferência por outra, não ganho de base
própria. Em São Paulo o FPM desceu até 2019 e voltou: hoje pesa quase o mesmo que em 2002. Parte da volta é
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
retrato (só São Paulo e Maranhão nos quatro anos), a dependência do município de até 10 mil habitantes ficou
entre 87,1% e 88,3% em São Paulo e entre 95,2% e 95,7% no Maranhão. O peso do FPM subiu de 33,6% para 36,0% no
paulista e caiu de 30,3% para 27,3% no maranhense; a EC 112/2021 explica parte da subida paulista.

11.8. **Triênio 2023 a 2025.** O GPT refez as comparações entre São Paulo e Maranhão com a média de três anos,
em reais de 2025, no painel de 830 municípios com contas utilizáveis nos três anos (617 paulistas e 213
maranhenses). Eu refiz com as bases remontadas e os números batem:

| Comparação, São Paulo contra Maranhão | Só 2024 | Média de 2023 a 2025 |
|---|---|---|
| Dependência a tamanho igual, até 50 mil hab. (pontos a mais no MA) | 13,5 | 13,6 (12,8 a 14,5) |
| Transferências por habitante, 5 a 50 mil hab. (SP em relação ao MA) | -11,6% | -9,5% (-12,2% a -6,7%) |
| Idem, até 5 mil hab. | -3,0% | -1,5% (-16,6% a +16,3%) |
| FPM como maior fatia em SP; FUNDEB no MA | 53,2%; 89,3% | 52,2%; 90,1% |
| Verba estadual, medida restrita, até 50 mil hab. (pontos a mais em SP) | 2,3 | 2,1 (1,9 a 2,3) |
| Verba federal, medida restrita (pontos a menos em SP) | 0,9 | 1,0 (0,7 a 1,3) |

As conclusões entre os dois estados não dependem do ano. Serve como faixa, não como número novo: 2023 e 2025
não passaram pela mesma conferência de 2024. Para as regiões não há triênio: 2023 só tem São Paulo e Maranhão,
e a base de 2025 ainda não tem Minas, Espírito Santo e Rio. O investimento mediano por habitante em São Paulo,
em reais de 2025, foi de R$ 640 em 2023, R$ 565 em 2024 e R$ 376 em 2025: 2024 não aparece como pico.

Figuras: `21_` a `29_` (painel de 2022 a 2025, SP e MA), `41_` a `49_` (série longa, de 2000 a 2025, sem 2008)
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

13.1. Há igualdade, mas só nas pontas da curva. No conjunto de todos os municípios, as frações de São Paulo e
do Maranhão só se igualam em zero, com corte acima de 99,8%. Entre os municípios de até 20 mil habitantes, as
duas são 100% com qualquer corte até 50,1%; até 10.188 habitantes, com qualquer corte até 62,5%; até 5 mil
habitantes, com qualquer corte até 66,0%. Esses limites são a menor dependência entre os paulistas de cada
recorte. Daí para cima a fração paulista cai e a maranhense não, e as curvas não se cruzam de novo antes de
zerar.

13.2. Essa igualdade é vazia de conteúdo. Ela diz que todo município pequeno dos dois estados recebe mais da
metade da receita de fora. Isso vale para quase todo município pequeno do país e é desenho do federalismo
fiscal brasileiro: o imposto se arrecada onde está a atividade econômica e se redistribui por fórmula. Uma
classe em que cabem todos não separa ninguém. Assim que o corte passa a separar, separa a favor da tese
contrária: com 80%, 82% dos paulistas e 98% dos maranhenses de até 20 mil habitantes; com 90%, 24% e 94%.

13.3. Entre as regiões, nos municípios de até 20 mil habitantes, a curva do Sudeste fica 0,1 ponto acima da do
Nordeste com cortes de 50% a 61%. A diferença é de um ou dois municípios nordestinos com dependência baixa, e
as duas frações estão acima de 99,5%. Não é resultado.

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
micromunicípios paulistas é anterior a 1988.

14.2. **Tamanho, custo e escala** (`escala-urbana.md`; seção 12). A pergunta do dono: a população é variável
substituta das outras, ou são coisas separadas? Os expoentes do logaritmo de cada grandeza contra o da
população, nos 3.356 municípios: PIB 1,14; tributos próprios 1,22; ISS 1,27; IPTU 1,68; FPM 0,52;
transferências 0,77; Câmara e administração 0,75. A economia só cresce mais que a população acima de uns 50 mil
habitantes (até aí o expoente do PIB é 1,01). A máquina é custo fixo: expoente 0,14 até 5 mil habitantes e 0,98
acima de 50 mil. Um FPM proporcional à população dentro de cada estado explicaria 68% do excesso de
transferências por habitante do município minúsculo e 21% da queda da dependência em parcela da receita. Tamanho
não fecha a conta entre os dois estados: dos 14,8 pontos de distância (843 municípios, todos os tamanhos),
sobram 11,9 com população e PIB por habitante. Limite: município não é cidade, e expoente de corte transversal
não é lei.

14.3. **A emenda segue a cadeira** (`representacao.md`; seção 13). O nome técnico é desproporcionalidade da
representação (*malapportionment*). Pelo índice de Loosemore-Hanby com o Censo 2022, 10,4% na Câmara e 37,4% no
Senado (conta própria; a tabela de cadeiras por estado não foi conferida em fonte oficial). Razão entre cadeiras
e população na Câmara: Norte 1,48; Nordeste 1,09; Sudeste 0,84. A São Paulo faltam 42 cadeiras. Pela regra de
2025, a emenda dá R$ 73 por habitante em São Paulo, R$ 193 no Maranhão e R$ 1.463 em Roraima, e essa ordem tem
correlação de 0,81 com a mediana municipal da seção 6. A sobrerrepresentação é do Norte de estados pequenos e do
Senado, não do Nordeste como bloco.

14.4. **Emendas no tempo** (`emendas-linha-do-tempo.md`; seção 14). A preços de 2025, o empenhado foi de R$ 17,5
bilhões em 2018 para R$ 47,1 bilhões em 2025. A transferência especial ("emenda Pix") foi de R$ 0,8 bilhão em
2020 para R$ 8,1 bilhões em 2024. A série do Portal da Transparência só serve de 2018 em diante, e 2026 é
parcial.

14.5. **A nota técnica do CEM** (`cem-nt23.md`; seção 15). O par R$ 1.816 contra R$ 393 por habitante soma só FPM
e FUNDEB. A nota nega propor fusão de municípios (p. 4) e não tem dado de emenda. Na base de 2024, por morador:
a União manda 3,3 vezes mais ao município de até 31 mil habitantes que ao de mais de 175 mil, e a emenda é 6,4
vezes maior; somando toda a receita, R$ 6.373 contra R$ 5.623, 13% a mais. Quem menos tem é o município grande
do Nordeste: R$ 4.300 por morador, contra R$ 6.118 no grande do Sudeste.

14.6. **O debate público** (`debate-publico.md`; seção 16). Os tributos próprios não cobrem a Câmara e a
administração em 2.598 dos 3.356 municípios, onde mora 29,7% da população. A receita por habitante do município
de até 5 mil habitantes é a maior de todas as faixas (R$ 9.647 por morador). A Frente Nacional de Prefeitas e
Prefeitos, em matéria da BBC, diz que cerca de 19% dos municípios têm 80% ou mais da receita vinda de fora; a
seção 13 dá 70,1% no Sudeste e 93,2% no Nordeste. Os dois números não cabem juntos e a definição do primeiro não
foi localizada: nenhum deve ser citado contra o outro antes de abrir a fonte.

14.7. **As saídas** (`solucoes-e-ia.md`; seção 17). Levar a máquina de todos os municípios de até 5 mil
habitantes ao custo da faixa de 20 a 50 mil economizaria, no teto, R$ 2,35 bilhões por ano: 0,28% da receita
municipal das duas regiões. A PEC 188/2019 foi arquivada em dezembro de 2022. A LC 230/2026 só trata de
desmembrar parte de um município para o vizinho (conferida por artigo jurídico, não pelo texto oficial).

Os scripts dessas contas estão em `docs/pesquisa/apoio/`. Em 06/10/2026 foram rodados de novo sobre a base
corrigida pela rodada 1: os números batem, com diferença na quarta casa dos expoentes e de R$ 2 na receita por
morador do município grande.

## O que ainda não se sabe

- Emenda e convênio estaduais por município e por programa, em São Paulo e no Maranhão. Desde o orçamento de
  2026 o STF estendeu a rastreabilidade às emendas estaduais (ADPF 854, segundo o Grok; não conferido), o que
  pode tornar esse dado disponível.
- Emenda federal por instrumento: empenhado do exercício contra restos a pagar, e por beneficiário final.
- Quanto da cota do ICMS de cada município é devolução (valor adicionado) e quanto é rateio.
- Se 2024, ano de eleição municipal, distorce o retrato nos outros onze estados. Em São Paulo e no Maranhão não
  distorce (11.7 e 11.8); para os demais falta 2023, e 2025 ainda não tem Minas, Espírito Santo e Rio.
- Quanto pesa cada causa da concentração de municípios acima dos degraus do FPM (10.4). Um teste possível:
  comparar a prévia do Censo de dezembro de 2022, enviada ao TCU, com o resultado final.
- O custo da máquina numa medida que valha para todos os estados.
- A série conta a conta antes de 2022. A conta 1.7.1.8.04 é assistência social em 2018 e SUS de 2019 a 2021
  (achado do GPT), então cada plano de contas antigo precisa de regra própria. Não foi feito; o painel conta a
  conta começa em 2022.
- O efeito da reforma tributária. A cota municipal do IBS será 80% por população. Isso tira receita do
  município pequeno com usina ou indústria (Sandovalina, na região de Presidente Prudente, é o exemplo citado
  pelo Grok a partir de simulação do IPEA de 2023; não conferido). O município pequeno sem valor adicionado,
  que é o caso típico do oeste paulista, tende a ganhar.
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
| "Transferências voluntárias" de 4,2% da receita no paulista pequeno | A medida tinha R$ 3,058 bilhões do SUS. Na restrita, 2,5%; o nome passou a "convênios e transferências de capital" (6) |
| "Três quartos do investimento" | 53% na medida restrita; 74% na ampla (6.4) |
| "O Maranhão recebe 0,0% do estado" | É mediana de lançamento: 84 de 127 lançaram zero; média de 0,24% (6.3) |
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
