# Resultado dos testes (2024)

Gerado por `src/mf/testes.py` a partir de `dados/processado/municipios_2024.parquet`. As hipóteses e as regras foram escritas antes, em `docs/HIPOTESES.md`. Efeito = grupo 1 menos grupo 2; o intervalo é de 95%; p (Holm) corrige as comparações múltiplas dentro da família. Nas linhas em log, o efeito está convertido em variação percentual. Nas comparações entre regiões, o p usado é o maior entre o robusto (HC3) e o agrupado por estado, porque os municípios de um mesmo estado se parecem e são só 13 estados. As linhas marcadas "pós-verificação" foram acrescentadas depois que a conferência independente mostrou que o efeito muda com o tamanho; não estavam no registro. Na família D, a medida restrita (sem o SUS de convênio e de capital e sem o convênio corrente estadual de educação) é a principal desde a revisão cruzada de 05/10/2026; a ampla é a do registro e fica como sensibilidade. A família S refaz A1 e C1 sem os municípios com `alerta_fpm` ou `alerta_fundeb`. A família R responde se o oeste paulista depende mais por ser oeste ou por ter município menor.

## A. Dependência em parcela da receita

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| A1-SP | Parcela de transferências na receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | -13,5 p.p. | -14,3 p.p. a -12,6 p.p. | < 0,001 | MA acima (exploratório) |
| A1-SP-5 | Parcela de transferências na receita: SP menos MA | 5 a 10 mil | 119 / 36 | -9,6 p.p. | -10,8 p.p. a -8,5 p.p. | < 0,001 | MA acima (exploratório) |
| A1-SP-10 | Parcela de transferências na receita: SP menos MA | 10 a 20 mil | 119 / 86 | -12,4 p.p. | -13,6 p.p. a -11,3 p.p. | < 0,001 | MA acima (exploratório) |
| A1-SP-20 | Parcela de transferências na receita: SP menos MA | 20 a 50 mil | 115 / 66 | -17,1 p.p. | -18,2 p.p. a -15,9 p.p. | < 0,001 | MA acima (exploratório) |
| A1-Su | Parcela de transferências na receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | -6,7 p.p. | -7,1 p.p. a -6,3 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| A1-Su-5 | Parcela de transferências na receita: Sudeste menos Nordeste | 5 a 10 mil | 367 / 351 | -4,9 p.p. | -5,5 p.p. a -4,2 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| A1-Su-10 | Parcela de transferências na receita: Sudeste menos Nordeste | 10 a 20 mil | 347 / 561 | -6,6 p.p. | -7,4 p.p. a -5,9 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| A1-Su-20 | Parcela de transferências na receita: Sudeste menos Nordeste | 20 a 50 mil | 280 / 400 | -10,9 p.p. | -12,0 p.p. a -9,8 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| A1b-SP | Idem, FPM e ICMS brutos e FUNDEB pelo saldo: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | -13,4 p.p. | -14,3 p.p. a -12,5 p.p. | < 0,001 | MA acima (exploratório) |
| A1b-Su | Idem, FPM e ICMS brutos e FUNDEB pelo saldo: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | -6,6 p.p. | -7,0 p.p. a -6,2 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| A2-SP | Tributos próprios sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | 10,4 p.p. | 9,8 p.p. a 11,1 p.p. | < 0,001 | SP acima (exploratório) |
| A2-SP-5 | Tributos próprios sobre a receita: SP menos MA | 5 a 10 mil | 119 / 36 | 7,7 p.p. | 6,9 p.p. a 8,5 p.p. | < 0,001 | SP acima (exploratório) |
| A2-SP-10 | Tributos próprios sobre a receita: SP menos MA | 10 a 20 mil | 119 / 86 | 9,5 p.p. | 8,6 p.p. a 10,4 p.p. | < 0,001 | SP acima (exploratório) |
| A2-SP-20 | Tributos próprios sobre a receita: SP menos MA | 20 a 50 mil | 115 / 66 | 12,9 p.p. | 11,9 p.p. a 13,9 p.p. | < 0,001 | SP acima (exploratório) |
| A2-Su | Tributos próprios sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | 5,1 p.p. | 4,8 p.p. a 5,5 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A2-Su-5 | Tributos próprios sobre a receita: Sudeste menos Nordeste | 5 a 10 mil | 367 / 351 | 3,6 p.p. | 3,1 p.p. a 4,2 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A2-Su-10 | Tributos próprios sobre a receita: Sudeste menos Nordeste | 10 a 20 mil | 347 / 561 | 5,0 p.p. | 4,4 p.p. a 5,5 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A2-Su-20 | Tributos próprios sobre a receita: Sudeste menos Nordeste | 20 a 50 mil | 280 / 400 | 8,1 p.p. | 7,4 p.p. a 8,9 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A3-SP | Tributos próprios sem o IR retido na fonte: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | 9,7 p.p. | 9,1 p.p. a 10,3 p.p. | < 0,001 | SP acima (exploratório) |
| A3-SP-5 | Tributos próprios sem o IR retido na fonte: SP menos MA | 5 a 10 mil | 119 / 36 | 7,0 p.p. | 6,2 p.p. a 7,8 p.p. | < 0,001 | SP acima (exploratório) |
| A3-SP-10 | Tributos próprios sem o IR retido na fonte: SP menos MA | 10 a 20 mil | 119 / 86 | 8,9 p.p. | 8,1 p.p. a 9,7 p.p. | < 0,001 | SP acima (exploratório) |
| A3-SP-20 | Tributos próprios sem o IR retido na fonte: SP menos MA | 20 a 50 mil | 115 / 66 | 11,7 p.p. | 10,8 p.p. a 12,7 p.p. | < 0,001 | SP acima (exploratório) |
| A3-Su | Tributos próprios sem o IR retido na fonte: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | 5,2 p.p. | 4,9 p.p. a 5,5 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A3-Su-5 | Tributos próprios sem o IR retido na fonte: Sudeste menos Nordeste | 5 a 10 mil | 367 / 351 | 3,7 p.p. | 3,2 p.p. a 4,2 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A3-Su-10 | Tributos próprios sem o IR retido na fonte: Sudeste menos Nordeste | 10 a 20 mil | 347 / 561 | 5,0 p.p. | 4,5 p.p. a 5,6 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| A3-Su-20 | Tributos próprios sem o IR retido na fonte: Sudeste menos Nordeste | 20 a 50 mil | 280 / 400 | 8,0 p.p. | 7,3 p.p. a 8,6 p.p. | < 0,001 | Sudeste acima (confirmatório) |

## B. Dependência por habitante

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| B1-SP | Transferências por habitante: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | -9,3% | -12,3% a -6,1% | < 0,001 | MA acima (exploratório) |
| B1-SP-5 | Transferências por habitante: SP menos MA | 5 a 10 mil | 119 / 36 | R$ -546 | R$ -1.006 a R$ -113 | 0,057 | diferença não distinguível de zero (exploratório) |
| B1-SP-10 | Transferências por habitante: SP menos MA | 10 a 20 mil | 119 / 86 | R$ -613 | R$ -887 a R$ -367 | < 0,001 | MA acima (exploratório) |
| B1-SP-20 | Transferências por habitante: SP menos MA | 20 a 50 mil | 115 / 66 | R$ -686 | R$ -925 a R$ -477 | < 0,001 | MA acima (exploratório) |
| B1-Su | Transferências por habitante: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | -3,1% | -4,8% a -1,3% | 1,000 | diferença não distinguível de zero (confirmatório) |
| B1-Su-5 | Transferências por habitante: Sudeste menos Nordeste | 5 a 10 mil | 367 / 351 | R$ -323 | R$ -496 a R$ -147 | 0,003 | Nordeste acima (confirmatório) |
| B1-Su-10 | Transferências por habitante: Sudeste menos Nordeste | 10 a 20 mil | 347 / 561 | R$ -483 | R$ -612 a R$ -360 | < 0,001 | Nordeste acima (confirmatório) |
| B1-Su-20 | Transferências por habitante: Sudeste menos Nordeste | 20 a 50 mil | 280 / 400 | R$ -197 | R$ -334 a R$ -68 | 0,015 | Nordeste acima (confirmatório) |
| B1x-SP-até | Transferências por habitante: SP menos MA, a tamanho igual | até 5 mil hab. | 138 / 5 | -3,1% | -18,1% a 14,8% | 1,000 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| B1x-Su-até | Transferências por habitante: Sudeste menos Nordeste, a tamanho igual | até 5 mil hab. | 382 / 239 | -0,6% | -3,2% a 2,1% | 1,000 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| B1x-SP-5 | Transferências por habitante: SP menos MA, a tamanho igual | 5 a 50 mil hab. | 353 / 188 | -11,6% | -14,4% a -8,7% | < 0,001 | MA acima (exploratório (pós-verificação)) |
| B1x-Su-5 | Transferências por habitante: Sudeste menos Nordeste, a tamanho igual | 5 a 50 mil hab. | 994 / 1312 | -5,0% | -6,9% a -3,2% | 1,000 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| B3 | Transferências por habitante: Sudeste até 5 mil hab. menos Nordeste de 10 a 20 mil hab. | faixas diferentes | 382 / 561 | R$ 3.350 | R$ 3.099 a R$ 3.614 | < 0,001 | Sudeste até 5 mil acima (confirmatório) |

## C. A maior fatia

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| C1-SP | Proporção com o FPM como maior fatia (especificação principal): SP menos MA | todos | 628 / 215 | 46,2 p.p. | 40,5 p.p. a 50,9 p.p. | < 0,001 | SP acima (exploratório) |
| C2-SP | Proporção com o FUNDEB como maior fatia (especificação principal): SP menos MA | todos | 628 / 215 | -88,0 p.p. | -91,5 p.p. a -83,0 p.p. | < 0,001 | MA acima (exploratório) |
| Cb1-SP | Proporção com o FPM como maior fatia (FUNDEB pelo saldo): SP menos MA | todos | 628 / 215 | 19,9 p.p. | 12,2 p.p. a 27,1 p.p. | < 0,001 | SP acima (exploratório) |
| Cb2-SP | Proporção com o FUNDEB como maior fatia (FUNDEB pelo saldo): SP menos MA | todos | 628 / 215 | -60,0 p.p. | -66,3 p.p. a -53,3 p.p. | < 0,001 | MA acima (exploratório) |
| C1-Su | Proporção com o FPM como maior fatia (especificação principal): Sudeste menos Nordeste | todos | 1633 / 1723 | 18,4 p.p. | 15,1 p.p. a 21,7 p.p. | < 0,001 | Sudeste acima (confirmatório) |
| C2-Su | Proporção com o FUNDEB como maior fatia (especificação principal): Sudeste menos Nordeste | todos | 1633 / 1723 | -44,9 p.p. | -47,3 p.p. a -42,4 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| Cb1-Su | Proporção com o FPM como maior fatia (FUNDEB pelo saldo): Sudeste menos Nordeste | todos | 1633 / 1723 | -7,5 p.p. | -10,5 p.p. a -4,4 p.p. | < 0,001 | Nordeste acima (confirmatório) |
| Cb2-Su | Proporção com o FUNDEB como maior fatia (FUNDEB pelo saldo): Sudeste menos Nordeste | todos | 1633 / 1723 | -17,4 p.p. | -19,3 p.p. a -15,7 p.p. | < 0,001 | Nordeste acima (confirmatório) |

## D. Convênio, pleito e emenda

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| D1-SP | Convênios e transferências de capital, medida restrita, sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | 1,5 p.p. | 1,0 p.p. a 1,9 p.p. | < 0,001 | SP acima (exploratório (pós-verificação)) |
| D1-SP-5 | Convênios e transferências de capital, medida restrita, sobre a receita: SP menos MA | 5 a 10 mil | 119 / 36 | 2,3 p.p. | 1,5 p.p. a 3,0 p.p. | < 0,001 | SP acima (exploratório (pós-verificação)) |
| D1-SP-10 | Convênios e transferências de capital, medida restrita, sobre a receita: SP menos MA | 10 a 20 mil | 119 / 86 | 1,8 p.p. | 1,2 p.p. a 2,3 p.p. | < 0,001 | SP acima (exploratório (pós-verificação)) |
| D1-SP-20 | Convênios e transferências de capital, medida restrita, sobre a receita: SP menos MA | 20 a 50 mil | 115 / 66 | 0,7 p.p. | 0,2 p.p. a 1,2 p.p. | 0,046 | SP acima (exploratório (pós-verificação)) |
| D1-Su | Convênios e transferências de capital, medida restrita, sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | 0,8 p.p. | 0,5 p.p. a 1,1 p.p. | 0,227 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| D1-Su-5 | Convênios e transferências de capital, medida restrita, sobre a receita: Sudeste menos Nordeste | 5 a 10 mil | 367 / 351 | 1,1 p.p. | 0,7 p.p. a 1,5 p.p. | < 0,001 | Sudeste acima (exploratório (pós-verificação)) |
| D1-Su-10 | Convênios e transferências de capital, medida restrita, sobre a receita: Sudeste menos Nordeste | 10 a 20 mil | 347 / 561 | 1,1 p.p. | 0,7 p.p. a 1,4 p.p. | < 0,001 | Sudeste acima (exploratório (pós-verificação)) |
| D1-Su-20 | Convênios e transferências de capital, medida restrita, sobre a receita: Sudeste menos Nordeste | 20 a 50 mil | 280 / 400 | 0,3 p.p. | 0,0 p.p. a 0,7 p.p. | 0,066 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| D1u-SP | Medida restrita, verba da União, sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | -0,9 p.p. | -1,3 p.p. a -0,5 p.p. | < 0,001 | MA acima (exploratório (pós-verificação)) |
| D1u-Su | Medida restrita, verba da União, sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | -1,3 p.p. | -1,5 p.p. a -1,1 p.p. | 0,066 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| D1e-SP | Medida restrita, verba do estado, sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | 2,3 p.p. | 2,1 p.p. a 2,5 p.p. | < 0,001 | SP acima (exploratório (pós-verificação)) |
| D1e-Su | Medida restrita, verba do estado, sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | 2,1 p.p. | 1,9 p.p. a 2,3 p.p. | < 0,001 | Sudeste acima (exploratório (pós-verificação)) |
| D1am-SP | Convênios e transferências de capital, medida ampla, sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | 3,5 p.p. | 2,9 p.p. a 4,1 p.p. | < 0,001 | SP acima (exploratório) |
| D1am-Su | Convênios e transferências de capital, medida ampla, sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | 1,7 p.p. | 1,4 p.p. a 2,0 p.p. | 0,003 | Sudeste acima (confirmatório) |
| D1uam-SP | Medida ampla, verba da União, sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | -1,0 p.p. | -1,4 p.p. a -0,6 p.p. | < 0,001 | MA acima (exploratório (pós-verificação)) |
| D1uam-Su | Medida ampla, verba da União, sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | -1,4 p.p. | -1,6 p.p. a -1,1 p.p. | 0,066 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| D1eam-SP | Medida ampla, verba do estado, sobre a receita: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | 4,4 p.p. | 4,0 p.p. a 4,8 p.p. | < 0,001 | SP acima (exploratório (pós-verificação)) |
| D1eam-Su | Medida ampla, verba do estado, sobre a receita: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | 3,1 p.p. | 2,8 p.p. a 3,3 p.p. | < 0,001 | Sudeste acima (exploratório (pós-verificação)) |
| D3-SP | Emendas federais pagas em 2025 por habitante: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | R$ -240 | R$ -278 a R$ -203 | < 0,001 | MA acima (exploratório) |
| D3-SP-5 | Emendas federais pagas em 2025 por habitante: SP menos MA | 5 a 10 mil | 119 / 36 | R$ -291 | R$ -395 a R$ -195 | < 0,001 | MA acima (exploratório) |
| D3-SP-10 | Emendas federais pagas em 2025 por habitante: SP menos MA | 10 a 20 mil | 119 / 86 | R$ -193 | R$ -248 a R$ -142 | < 0,001 | MA acima (exploratório) |
| D3-SP-20 | Emendas federais pagas em 2025 por habitante: SP menos MA | 20 a 50 mil | 115 / 66 | R$ -167 | R$ -216 a R$ -122 | < 0,001 | MA acima (exploratório) |
| D3-Su | Emendas federais pagas em 2025 por habitante: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | R$ -235 | R$ -256 a R$ -213 | < 0,001 | Nordeste acima (confirmatório) |
| D3-Su-5 | Emendas federais pagas em 2025 por habitante: Sudeste menos Nordeste | 5 a 10 mil | 367 / 351 | R$ -239 | R$ -271 a R$ -206 | < 0,001 | Nordeste acima (confirmatório) |
| D3-Su-10 | Emendas federais pagas em 2025 por habitante: Sudeste menos Nordeste | 10 a 20 mil | 347 / 561 | R$ -122 | R$ -143 a R$ -100 | < 0,001 | Nordeste acima (confirmatório) |
| D3-Su-20 | Emendas federais pagas em 2025 por habitante: Sudeste menos Nordeste | 20 a 50 mil | 280 / 400 | R$ -92 | R$ -111 a R$ -74 | < 0,001 | Nordeste acima (confirmatório) |

## E. Custo da máquina

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| E1-todos | Elasticidade do gasto por habitante com a máquina em relação à população: Nordeste e Sudeste | todos | 3356 / 0 | -0,275 | -0,293 a -0,257 | < 0,001 | cai com o tamanho (confirmatório) |
| E1-SP | Elasticidade do gasto por habitante com a máquina em relação à população: SP | todos | 628 / 0 | -0,227 | -0,259 a -0,195 | < 0,001 | cai com o tamanho (exploratório) |
| E1-MA | Elasticidade do gasto por habitante com a máquina em relação à população: MA | todos | 215 / 0 | -0,309 | -0,381 a -0,238 | < 0,001 | cai com o tamanho (exploratório) |
| E1-SE | Elasticidade do gasto por habitante com a máquina em relação à população: Sudeste | todos | 1633 / 0 | -0,254 | -0,277 a -0,232 | < 0,001 | cai com o tamanho (confirmatório) |
| E1-NE | Elasticidade do gasto por habitante com a máquina em relação à população: Nordeste | todos | 1723 / 0 | -0,312 | -0,344 a -0,281 | < 0,001 | cai com o tamanho (confirmatório) |
| E1t-até | Elasticidade do gasto por habitante com a máquina, por trecho | até 5 mil hab. | 621 / 0 | -0,908 | -0,997 a -0,818 | < 0,001 | cai com o tamanho (exploratório (pós-verificação)) |
| E1t-5 | Elasticidade do gasto por habitante com a máquina, por trecho | 5 a 20 mil hab. | 1626 / 0 | -0,404 | -0,453 a -0,355 | < 0,001 | cai com o tamanho (exploratório (pós-verificação)) |
| E1t-20 | Elasticidade do gasto por habitante com a máquina, por trecho | 20 a 100 mil hab. | 897 / 0 | -0,067 | -0,137 a 0,002 | 0,117 | sem evidência (exploratório (pós-verificação)) |
| E1t-maisde | Elasticidade do gasto por habitante com a máquina, por trecho | mais de 100 mil hab. | 212 / 0 | -0,133 | -0,209 a -0,057 | 0,003 | cai com o tamanho (exploratório (pós-verificação)) |
| E2-SP | Gasto por habitante com Câmara e administração: SP menos MA, a tamanho igual | até 50 mil hab. | 491 / 193 | -8,0% | -13,7% a -2,0% | 0,029 | MA acima (exploratório) |
| E2-Su | Gasto por habitante com Câmara e administração: Sudeste menos Nordeste, a tamanho igual | até 50 mil hab. | 1376 / 1551 | -2,3% | -5,7% a 1,1% | 0,812 | diferença não distinguível de zero (confirmatório) |
| E2q-SP | Gasto por habitante com Câmara e administração: SP menos MA, mediana a tamanho igual | até 50 mil hab. | 491 / 193 | -11,8% | -18,3% a -4,8% | 0,005 | MA acima (exploratório (pós-verificação)) |
| E2q-Su | Gasto por habitante com Câmara e administração: Sudeste menos Nordeste, mediana a tamanho igual | até 50 mil hab. | 1376 / 1551 | -7,0% | -10,6% a -3,4% | 0,001 | Nordeste acima (exploratório (pós-verificação)) |
| E3-SP | Proporção em que os tributos próprios não cobrem a máquina: SP menos MA | todos | 628 / 215 | -52,2 p.p. | -56,5 p.p. a -46,9 p.p. | < 0,001 | MA acima (exploratório) |
| E3-Su | Proporção em que os tributos próprios não cobrem a máquina: Sudeste menos Nordeste | todos | 1633 / 1723 | -26,2 p.p. | -28,9 p.p. a -23,5 p.p. | < 0,001 | Nordeste acima (confirmatório) |

## F. Limiares do FPM

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| F1 | Fração dos municípios vizinhos de um limiar do FPM que está logo acima dele (Censo 2022, NE e SE) | 17 limiares | 395 / 125 | 76,0% | 72,1% a 79,4% | < 0,001 | há excesso acima do limiar (confirmatório) |

## R. São Paulo por região, a tamanho igual (seção 12)

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| R1 | Parcela de transferências na receita: quatro regiões do oeste paulista menos o resto do estado, a tamanho igual | SP, até 50 mil hab. | 223 / 268 | 0,9 p.p. | -0,2 p.p. a 2,0 p.p. | 0,188 | diferença não distinguível de zero (exploratório (pós-verificação)) |
| R2 | Idem, só municípios de 5 a 10 mil habitantes | SP, 5 a 10 mil hab. | 57 / 62 | 0,4 p.p. | -1,3 p.p. a 2,4 p.p. | 0,680 | diferença não distinguível de zero (exploratório (pós-verificação)) |

## S. Sensibilidade: sem municípios com alerta de FPM ou de FUNDEB

| id | afirmação | recorte | n1 / n2 | efeito | intervalo de 95% | p (Holm) | leitura |
|---|---|---|---|---|---|---|---|
| A1-SP-sa | Parcela de transferências na receita: SP menos MA, a tamanho igual, sem municípios com alerta | até 50 mil hab. | 484 / 186 | -13,4 p.p. | -14,2 p.p. a -12,5 p.p. | < 0,001 | MA acima (sensibilidade (pós-verificação)) |
| C1-SP-sa | Proporção com o FPM como maior fatia: SP menos MA, sem municípios com alerta | todos | 619 / 205 | 46,0 p.p. | 40,1 p.p. a 50,8 p.p. | < 0,001 | SP acima (sensibilidade (pós-verificação)) |
| A1-Su-sa | Parcela de transferências na receita: Sudeste menos Nordeste, a tamanho igual, sem municípios com alerta | até 50 mil hab. | 1355 / 1480 | -6,7 p.p. | -7,1 p.p. a -6,3 p.p. | < 0,001 | Nordeste acima (sensibilidade (pós-verificação)) |
| C1-Su-sa | Proporção com o FPM como maior fatia: Sudeste menos Nordeste, sem municípios com alerta | todos | 1608 / 1648 | 18,6 p.p. | 15,2 p.p. a 21,9 p.p. | < 0,001 | Sudeste acima (sensibilidade (pós-verificação)) |

## G. Evolução no tempo (2002 a 2025, municípios de até 20 mil habitantes)

Série longa do IPEADATA (receita bruta). Gerado por `src/mf/testes_tempo.py`. Efeito em pontos percentuais; intervalo de 95%; p com correção de Holm dentro da família.

| id | afirmação | tipo | n | início | fim | efeito (p.p.) | intervalo de 95% | p (Holm) |
|---|---|---|---|---|---|---|---|---|
| G-dep_corrente-SP | Transferências correntes sobre a receita corrente: 2025 menos 2002, SP | dentro do município | 378 | 89,1% | 86,3% | -2,7 | -3,2 a -2,2 | < 0,001 |
| Gt-dep_corrente-SP | Transferências correntes sobre a receita corrente: tendência por década, SP | efeito fixo de município | 393 | – | – | -0,9 | -1,2 a -0,7 | < 0,001 |
| G-dep_corrente-MA | Transferências correntes sobre a receita corrente: 2025 menos 2002, MA | dentro do município | 102 | 97,8% | 94,5% | -3,2 | -4,2 a -2,8 | < 0,001 |
| Gt-dep_corrente-MA | Transferências correntes sobre a receita corrente: tendência por década, MA | efeito fixo de município | 129 | – | – | -1,1 | -1,4 a -0,8 | < 0,001 |
| G-dep_corrente-Sudeste | Transferências correntes sobre a receita corrente: 2025 menos 2002, Sudeste | dentro do município | 1.097 | 92,3% | 88,7% | -3,1 | -3,3 a -2,7 | < 0,001 |
| Gt-dep_corrente-Sudeste | Transferências correntes sobre a receita corrente: tendência por década, Sudeste | efeito fixo de município | 1.128 | – | – | -1,0 | -1,1 a -0,8 | < 0,001 |
| G-dep_corrente-Nordeste | Transferências correntes sobre a receita corrente: 2025 menos 2002, Nordeste | dentro do município | 1.111 | 96,7% | 93,0% | -3,4 | -3,6 a -3,2 | < 0,001 |
| Gt-dep_corrente-Nordeste | Transferências correntes sobre a receita corrente: tendência por década, Nordeste | efeito fixo de município | 1.201 | – | – | -1,5 | -1,6 a -1,3 | < 0,001 |
| Gd-dep_corrente | Transferências correntes sobre a receita corrente: a mudança de 2002 a 2025 no Sudeste menos a do Nordeste | diferença das diferenças | 2.208 | – | – | 0,6 | 0,3 a 1,0 | 0,003 |
| G-pct_fpm_rc-SP | FPM sobre a receita corrente: 2025 menos 2002, SP | dentro do município | 378 | 37,3% | 35,5% | -1,6 | -2,1 a -0,9 | < 0,001 |
| Gt-pct_fpm_rc-SP | FPM sobre a receita corrente: tendência por década, SP | efeito fixo de município | 393 | – | – | -1,3 | -1,6 a -1,1 | < 0,001 |
| G-pct_fpm_rc-MA | FPM sobre a receita corrente: 2025 menos 2002, MA | dentro do município | 102 | 52,8% | 28,9% | -23,2 | -24,9 a -21,3 | < 0,001 |
| Gt-pct_fpm_rc-MA | FPM sobre a receita corrente: tendência por década, MA | efeito fixo de município | 129 | – | – | -9,3 | -10,0 a -8,7 | < 0,001 |
| G-pct_fpm_rc-Sudeste | FPM sobre a receita corrente: 2025 menos 2002, Sudeste | dentro do município | 1.097 | 49,7% | 40,9% | -6,5 | -7,2 a -6,0 | < 0,001 |
| Gt-pct_fpm_rc-Sudeste | FPM sobre a receita corrente: tendência por década, Sudeste | efeito fixo de município | 1.128 | – | – | -3,3 | -3,5 a -3,1 | < 0,001 |
| G-pct_fpm_rc-Nordeste | FPM sobre a receita corrente: 2025 menos 2002, Nordeste | dentro do município | 1.111 | 52,6% | 36,3% | -16,1 | -16,6 a -15,4 | < 0,001 |
| Gt-pct_fpm_rc-Nordeste | FPM sobre a receita corrente: tendência por década, Nordeste | efeito fixo de município | 1.201 | – | – | -6,7 | -6,9 a -6,5 | < 0,001 |
| Gd-pct_fpm_rc | FPM sobre a receita corrente: a mudança de 2002 a 2025 no Sudeste menos a do Nordeste | diferença das diferenças | 2.208 | – | – | 9,4 | 8,7 a 10,2 | < 0,001 |
| G-pct_icms_rc-SP | Cota-parte do ICMS sobre a receita corrente: 2025 menos 2002, SP | dentro do município | 378 | 26,2% | 20,9% | -5,4 | -5,9 a -4,9 | < 0,001 |
| Gt-pct_icms_rc-SP | Cota-parte do ICMS sobre a receita corrente: tendência por década, SP | efeito fixo de município | 393 | – | – | -2,8 | -3,1 a -2,5 | < 0,001 |
| G-pct_icms_rc-MA | Cota-parte do ICMS sobre a receita corrente: 2025 menos 2002, MA | dentro do município | 102 | 4,7% | 9,6% | 4,9 | 4,1 a 6,0 | < 0,001 |
| Gt-pct_icms_rc-MA | Cota-parte do ICMS sobre a receita corrente: tendência por década, MA | efeito fixo de município | 129 | – | – | 1,9 | 1,4 a 2,4 | < 0,001 |
| G-pct_icms_rc-Sudeste | Cota-parte do ICMS sobre a receita corrente: 2025 menos 2002, Sudeste | dentro do município | 1.096 | 18,9% | 15,0% | -3,8 | -4,1 a -3,4 | < 0,001 |
| Gt-pct_icms_rc-Sudeste | Cota-parte do ICMS sobre a receita corrente: tendência por década, Sudeste | efeito fixo de município | 1.128 | – | – | -2,0 | -2,2 a -1,9 | < 0,001 |
| G-pct_icms_rc-Nordeste | Cota-parte do ICMS sobre a receita corrente: 2025 menos 2002, Nordeste | dentro do município | 1.111 | 8,0% | 7,8% | -0,4 | -0,7 a 0,0 | 0,719 |
| Gt-pct_icms_rc-Nordeste | Cota-parte do ICMS sobre a receita corrente: tendência por década, Nordeste | efeito fixo de município | 1.201 | – | – | 0,3 | 0,2 a 0,5 | < 0,001 |
| Gd-pct_icms_rc | Cota-parte do ICMS sobre a receita corrente: a mudança de 2002 a 2025 no Sudeste menos a do Nordeste | diferença das diferenças | 2.207 | – | – | -4,1 | -4,5 a -3,6 | < 0,001 |
| G-maquina_rc-SP | Câmara e administração sobre a receita corrente: 2025 menos 2002, SP | dentro do município | 378 | 18,3% | 13,1% | -4,6 | -5,2 a -4,1 | < 0,001 |
| Gt-maquina_rc-SP | Câmara e administração sobre a receita corrente: tendência por década, SP | efeito fixo de município | 393 | – | – | -1,9 | -2,2 a -1,6 | < 0,001 |
| G-maquina_rc-MA | Câmara e administração sobre a receita corrente: 2025 menos 2002, MA | dentro do município | 102 | 21,0% | 14,7% | -6,7 | -8,2 a -4,5 | < 0,001 |
| Gt-maquina_rc-MA | Câmara e administração sobre a receita corrente: tendência por década, MA | efeito fixo de município | 129 | – | – | -1,6 | -2,2 a -1,1 | < 0,001 |
| G-maquina_rc-Sudeste | Câmara e administração sobre a receita corrente: 2025 menos 2002, Sudeste | dentro do município | 1.097 | 19,3% | 12,9% | -5,9 | -6,2 a -5,4 | < 0,001 |
| Gt-maquina_rc-Sudeste | Câmara e administração sobre a receita corrente: tendência por década, Sudeste | efeito fixo de município | 1.128 | – | – | -2,6 | -2,8 a -2,4 | < 0,001 |
| G-maquina_rc-Nordeste | Câmara e administração sobre a receita corrente: 2025 menos 2002, Nordeste | dentro do município | 1.111 | 19,7% | 14,0% | -5,6 | -6,3 a -5,2 | < 0,001 |
| Gt-maquina_rc-Nordeste | Câmara e administração sobre a receita corrente: tendência por década, Nordeste | efeito fixo de município | 1.201 | – | – | -1,6 | -2,7 a -0,6 | 0,007 |
| Gd-maquina_rc | Câmara e administração sobre a receita corrente: a mudança de 2002 a 2025 no Sudeste menos a do Nordeste | diferença das diferenças | 2.208 | – | – | -0,3 | -0,9 a 0,3 | 0,653 |
