# Método

Como os números deste estudo são feitos, do dado bruto à figura. Quem for conferir deve conseguir refazer cada
passo só com este arquivo e o código em `src/mf/`.

## Recorte

- Municípios dos nove estados do Nordeste e dos quatro do Sudeste: 3.462 pela lista do IBGE.
- Retrato: exercício de 2024. Série: 2022 a 2025 no mesmo plano de contas, com os 13 estados nos quatro anos
  (3.352, 3.360, 3.356 e 3.371 municípios utilizáveis). Os anos de 2013 a 2021 entram quando os planos de contas
  antigos forem mapeados; os dados de 2019 a 2021 já estão em disco.
- Vocabulário: receita externa é o que a União e o estado repassam (FPM, FUNDEB, cota do ICMS e do IPVA, SUS,
  royalties e outras transferências); receita interna, ou própria, é o que o município arrecada (tributos
  próprios e demais receitas próprias). Dependência é a soma das seis fontes externas sobre a receita.
- Grandes Regiões: as cinco do IBGE (Norte, Nordeste, Sudeste, Sul e Centro-Oeste). O estudo compara duas,
  Sudeste e Nordeste, com 13 estados. Nos textos do estudo, "região" sem adjetivo é sempre uma Grande Região.
- Região geográfica intermediária: divisão do IBGE de 2017, dentro de cada estado; substituiu a mesorregião.
  São Paulo tem 11 (São Paulo, Sorocaba, Bauru, Marília, Presidente Prudente, Araçatuba, São José do Rio Preto,
  Ribeirão Preto, Araraquara, Campinas e São José dos Campos) e o Maranhão, 5 (São Luís, Santa Inês-Bacabal,
  Caxias, Presidente Dutra e Imperatriz). Depois da primeira vez, "região intermediária"; nunca só "região".
- Região geográfica imediata: a divisão menor de 2017; substituiu a microrregião. O estudo não usa.
- Fonte das três definições: API de localidades do IBGE (`servicodados.ibge.gov.br/api/docs/localidades` e
  `/api/v1/localidades/estados/SP/regioes-intermediarias`), consultada em 06/10/2026, e o texto de divulgação do
  IBGE de 2017.
- Interior profundo não é divisão oficial. O que foi assumido: o oeste paulista são as quatro regiões
  intermediárias de Presidente Prudente, Marília, Araçatuba e São José do Rio Preto, medidas em conjunto; o Vale
  do Ribeira não tem região intermediária própria e aparece no mapa.

## Fontes

| O quê | De onde | Arquivo ou rotina |
|---|---|---|
| Contas anuais dos municípios (DCA), todos os anexos | API do SICONFI, Tesouro Nacional: `apidatalake.tesouro.gov.br/ords/siconfi/tt/dca`, uma chamada por município e ano | `src/mf/baixar_siconfi.py`, `baixar_fila.py` |
| Malha municipal, divisão regional, Censo 2010 e 2022, estimativas de população, PIB municipal, IPCA | IBGE (API de malhas, de localidades e SIDRA) | `src/mf/baixar_ibge.py` |
| Emendas federais pagas, por favorecido | Portal da Transparência, arquivo em lote de emendas | `docs/pesquisa/emendas.md`, `src/mf/extras.py` |
| CAPAG dos municípios (posição de 01/09/2026) | Tesouro Transparente | `docs/pesquisa/saude-fiscal.md` |
| IFGF por município, 2013 a 2024 | Firjan, edição 2025 | idem |
| Coeficientes do FPM por município, 2024 a 2026 | TCU, Decisões Normativas | `docs/pesquisa/fpm.md` |
| Cadeiras de deputado federal por estado | Câmara dos Deputados, página "Número de deputados por estado", conferida em 06/10/2026 (27 bancadas, soma 513) | `docs/pesquisa/representacao.md`, `dados/processado/representacao_uf.csv` |
| Área dos municípios (território por tamanho) | IBGE, Censo 2022, SIDRA 4714 | `revisao/claude/apoio/r3_territorio.py` |

A API do SICONFI recusa mais de cerca de uma requisição por segundo. O robô se ajusta sozinho a esse limite e
pode ser interrompido e retomado.

## Da DCA à "pizza" da receita

1. Usa-se o Anexo I-C (receitas orçamentárias). Ele traz todos os níveis do plano de contas, a conta-mãe e as
   filhas; somam-se só as folhas de cada município, para nada contar em dobro. A soma das folhas é igual à
   linha de total da própria DCA em todos os municípios (a declaração fecha por construção), então essa
   conferência não tira ninguém; quem sai, sai pelos crivos listados adiante.
2. Cada folha vale o valor bruto menos as três colunas de dedução (FUNDEB, transferências constitucionais e
   outras). Ou seja: o FPM e o ICMS entram já sem os 20% que vão para o FUNDEB, e o FUNDEB entra pelo que o
   município recebeu do fundo, complementação da União incluída. Isso depende de a prefeitura declarar a
   dedução; as que não declararam direito ficam fora (ver crivos).
3. Receitas intraorçamentárias ficam fora (são o município pagando a si mesmo).
4. Ficam fora da base, por não financiarem a prefeitura ou por não serem receita recorrente: as receitas do
   regime próprio de previdência (contribuições dos servidores, rendimento das aplicações do fundo,
   compensação entre regimes, aportes para déficit atuarial), as demais contribuições previdenciárias
   (1.2.1.9.50), as contribuições para assistência à saúde dos servidores (1.2.1.6) e a receita de serviço de
   assistência à saúde suplementar dos servidores (1.6.3.2.01, R$ 139 milhões em 6 municípios); as operações
   de crédito; a venda de bens; as demais receitas de capital que não são transferência; e as transferências
   de capital de instituições privadas (2.4.4), de pessoas físicas (2.4.9.1, R$ 2,2 milhões em 5 municípios) e
   do exterior (2.4.6). As privadas, em Minas, são reparação de mineração e chegam a 62% da receita de um
   município. Sem tirar a previdência, município com regime próprio pareceria mais "autônomo" que o vizinho
   que contribui para o INSS.
5. O que sobra é a **receita-base**, dividida em oito fatias:

| Fatia | O que entra (código de natureza da receita, plano de 2022) |
|---|---|
| Tributos próprios | Impostos, taxas e contribuição de melhoria (1.1: IPTU, ISS, ITBI, IR retido na fonte, taxas) e a contribuição de iluminação pública (1.2.4) |
| Demais receitas próprias | Outras contribuições, receita patrimonial (inclui juros das aplicações), serviços, outras receitas correntes e as transferências correntes de instituições privadas, de pessoas e do exterior (não são repasse da União nem do estado) |
| ICMS e IPVA | Participação na receita dos estados (1.7.2.1: ICMS, IPVA, IPI-exportação, CIDE) e o ICMS e o IPI que a prefeitura lançou como imposto próprio (1.1.1.4.50 e 1.1.1.4.01), ver nota adiante |
| Royalties | Compensações financeiras por petróleo, mineração e recursos hídricos (1.7.1.2 e 1.7.2.2), menos o Fundo Especial do Petróleo, que é rateado entre todos |
| FPM | 1.7.1.1.51, cota mensal e cotas extras |
| FUNDEB | Recebido do fundo (1.7.5.1) e complementação da União (1.7.1.5) |
| SUS | Só o fundo a fundo corrente da União e do estado (1.7.1.3 e 1.7.2.3) |
| Outras transferências | FNDE, FNAS, ITR, Fundo Especial do Petróleo, convênios, transferências especiais (emenda Pix), demais transferências correntes e todas as de capital, inclusive o SUS de convênio e de capital |

A tabela completa, código por código, está em `src/mf/classificar.py` (`REGRAS_2022` e `FATIA_DA_CATEGORIA`).

**O que é "SUS" na pizza.** A fatia SUS é o repasse fundo a fundo corrente. O SUS que chega por convênio ou
como transferência de capital fica em "outras transferências", em categorias próprias: convênio corrente da
União (1.7.1.7.50) e do estado (1.7.2.4.50), convênio de capital da União (2.4.1.4.50) e do estado (2.4.2.2.50),
capital fundo a fundo da União (2.4.1.1), do estado (2.4.2.1) e de outros municípios (2.4.3.1 e 2.4.3.2.50).
Somam R$ 3,493 bilhões em 2.339 municípios. A dependência não muda
com essa escolha; a maior fatia mudaria em até 10 municípios se tudo fosse para a fatia SUS.

**Imposto de outro ente lançado como próprio.** Município não cobra ICMS nem IPI. Onde a prefeitura lançou
ICMS (1.1.1.4.50.1 e .2) ou IPI (1.1.1.4.01.5) como imposto, o valor é tratado como cota recebida e vai para a
fatia "ICMS e IPVA". São 18 municípios e R$ 143,7 milhões; a dependência muda mais de 0,5 ponto em 12 deles
(até 8,4 pontos, em Salto/SP, que passa de "tributos próprios" para "ICMS e IPVA" como maior fatia). A coluna
`alerta_imposto_outro_ente` guarda o valor sobre a receita-base. O ITR lançado como imposto (1.1.1.2.01,
R$ 23,1 milhões em 40 municípios) continua tributo próprio: o município conveniado com a Receita Federal cobra
o imposto e fica com 100% dele. Não foi conferido, município a município, se os 40 têm convênio.

**Versão do ementário.** As regras foram escritas sobre o ementário da receita de 2024 (planilha "29.05" de
2024, segundo a réplica do GPT em `revisao/gpt/replica/ementario_oficial_2024.csv`; eu não reabri a planilha).
A conta 1.1.2.2.53 (taxa de resíduos, R$ 2,397 bilhões em 111 municípios, número do GPT) só aparece na síntese
de alterações do ementário; cai na regra geral de taxas.

### Crivos de plausibilidade

Um município entra na análise (`ok`) se entregou a DCA e passa por quatro crivos; o motivo de quem sai fica na
coluna `motivo_fora`. Em 2024 saíram 106 de 3.462 e ficaram 3.356.

| Crivo | Por quê | Fora em 2024 |
|---|---|---|
| Dedução do FUNDEB entre 10% e 25% da cesta (FPM, ICMS, IPVA, IPI, ITR); o normal é 18,6% | Há prefeitura que não declara a dedução, que a soma ao bruto ou que declara o líquido como bruto. O FPM e o saldo do FUNDEB dela saem errados | 93 (BA 25, PB 19, SP 17, MG 11) |
| Cesta do FUNDEB declarada | Sem FPM, ICMS, IPVA, IPI e ITR não há sobre o que conferir a dedução | 1 (Bandeira do Sul/MG) |
| Entregou a DCA | | 8 |
| Receita-base positiva | Declarou só deduções | 3 |
| Receita-base de pelo menos R$ 1.000 por habitante e FPM maior que zero | Declaração visivelmente incompleta | 1 |
| Nenhuma fatia abaixo de -0,5% da receita | Dedução lançada em conta diferente da do bruto | 0 além dos anteriores |

Onde a coluna "Deduções - FUNDEB" veio zerada e as outras colunas de dedução da cesta estão na faixa esperada,
elas valem como aporte ao FUNDEB.

### Alertas que marcam sem excluir

Vieram da revisão cruzada de 05/10/2026. O município continua na análise; a coluna serve para refazer a conta
sem ele. A contagem está em `docs/NUMEROS.md`, tabela "Alertas".

| Coluna | O que marca | Em 2024 |
|---|---|---|
| `alerta_fpm` | FPM bruto a mais de 5% da referência (cota do estado vezes o coeficiente efetivo do TCU). Lista do GPT, `revisao/gpt/anomalias/fpm_5pct.csv`; só existe para 2024 | 98 municípios, 54 com contas utilizáveis |
| `alerta_fundeb` | Aporte ao FUNDEB a mais de 2 pontos percentuais de 20% da cesta ordinária. Lista do GPT, `fundeb_exato_2pp.csv`; só 2024 | 155, 62 utilizáveis (27 no Piauí) |
| `alerta_imposto_outro_ente` | ICMS ou IPI lançado como imposto próprio, sobre a receita-base (número, não marca) | 18 |
| `alerta_capital_excepcional` | Uma só categoria de transferência de capital acima de 25% da receita-base | 7, 6 utilizáveis (Biquinhas/MG: 59%) |
| `alerta_fatia_negativa` | Alguma fatia abaixo de zero | 4, nenhum utilizável |

As duas listas do GPT não foram refeitas por mim: a referência do FPM depende da cota de cada estado, que não
está na base. A sensibilidade "sem municípios com alerta" (família S de `docs/TESTES.md`) refaz A1 e C1 sem os
100 municípios utilizáveis que têm `alerta_fpm` ou `alerta_fundeb`.

### Especificação alternativa

Toda conclusão é refeita com FPM, ICMS, IPVA e as demais cotas pelo valor bruto e o FUNDEB contado só pelo
saldo (recebido menos aportado, com piso em zero). Essa conta responde "de quem é o dinheiro na origem"; a
principal responde "o que entrou no caixa, com que rótulo". As colunas terminam em `_b`.

## Indicadores

| Nome na base | Conta |
|---|---|
| `dep_transf` | transferências correntes e de capital ÷ receita-base |
| `autonomia` | tributos próprios ÷ receita-base |
| `autonomia_sem_irrf` | idem, sem o imposto de renda retido na fonte, que é imposto federal sobre a folha do próprio município |
| `pct_voluntarias_restrita` | **medida principal da verba negociada**: convênios da União e do estado, transferências especiais e transferências de capital ÷ receita-base, sem o SUS (convênio corrente, convênio de capital e capital fundo a fundo) e sem o convênio corrente estadual de educação (1.7.2.4.51). Mede convênio e obra; não enxerga a emenda paga a fundo de saúde |
| `pct_vol_uniao_restrita`, `pct_vol_estado_restrita` | a mesma conta separada por quem paga |
| `voluntarias_restrita_sobre_invest` | a medida restrita ÷ investimento empenhado |
| `pct_voluntarias`, `pct_vol_uniao`, `pct_vol_estado` | medida ampla, a que o estudo usava até 05/10/2026: a restrita mais o SUS de convênio e de capital e o convênio corrente estadual de educação. No texto ela se chama "convênios e transferências de capital"; fica como sensibilidade. `pct_vol_estado_sem_saude_educ` é a ampla do estado sem os dois convênios correntes |
| `emenda_2025_pc`, `emenda_2025_sobre_base` | emendas federais pagas em 2025 a prefeituras e fundos municipais ÷ população, e ÷ receita-base do ano da linha (Portal da Transparência; não vem da DCA). Na base de 2024 o denominador é a receita de 2024 |
| `emenda_2025_sobre_base_2025` | a mesma emenda ÷ receita-base de 2025, onde a base de 2025 é utilizável (3.371 municípios, os 13 estados) |
| `rec_corrente_liq`, `poupanca_corrente` | receita líquida sem operação de crédito, venda de bens e toda transferência de capital, inclusive a de instituições privadas (corrigido em 06/10/2026, ver os limites); e (essa receita − despesa corrente) ÷ essa receita. Nenhum achado usa as duas colunas |
| `maquina_pc` | despesa empenhada nas funções 01 (Legislativa) e 04 (Administração) ÷ população |
| `proprios_sobre_maquina` | tributos próprios ÷ despesa nas funções 01 e 04 |
| `pessoal_sobre_base`, `invest_sobre_base` | despesa de pessoal (grupo 3.1) e investimentos (grupo 4.4) ÷ receita-base |
| `fundeb_saldo` | FUNDEB recebido, com complementação, menos o que o município aportou |
| `pec188` | menos de 5 mil habitantes e IPTU + ITBI + ISS abaixo de 10% da receita corrente líquida aproximada |
| `maior_fatia` | a fatia de maior peso na receita-base do município |

População das faixas: Censo 2022. Valores por habitante: estimativa do IBGE do ano (2024 em diante), Censo
(2022), média geométrica (2023) e interpolação entre os Censos de 2010 e 2022 (antes de 2022).

**Por que duas medidas de verba negociada.** A Lei de Responsabilidade Fiscal, art. 25, define transferência
voluntária como a que não decorre de determinação constitucional ou legal nem se destina ao SUS. A medida ampla
tinha R$ 3,493 bilhões do SUS dentro (2.339 municípios) e R$ 2,352 bilhões de convênio corrente estadual de
educação (1.286 municípios), que pode ser repasse regular e não pleito. A restrita tira os dois. Até 06/10/2026
a restrita ainda continha os convênios de capital para o SUS (2.4.1.4.50 e 2.4.2.2.50, R$ 435 milhões entre os
municípios utilizáveis); saíram na rodada 2 da revisão (achado do GPT), com categorias próprias em
`src/mf/classificar.py` (`convenios_uniao_cap_sus` e `convenios_estado_cap_sus`). Continuam na ampla e na
dependência. Nenhuma das duas é a "transferência voluntária" da lei: as duas contêm transferência de capital
que pode ser legal ou obrigatória. Por isso o texto fala em "convênios e transferências de capital".

O que a correção mudou: a verba estadual a tamanho igual entre São Paulo e Maranhão foi de +2,3 para +2,2
pontos (2,0 a 2,5); a mediana estadual paulista até 20 mil habitantes, de 2,54% para 2,45%; a verba negociada
sobre o investimento no paulista de até 5 mil habitantes, de 53% para 49%; as prefeituras maranhenses de até
20 mil habitantes com zero de verba estadual, de 84 para 90 de 127. Não mudaram a receita-base, as oito fatias,
a dependência, a maior fatia nem a medida ampla (`revisao/claude/r3/PIPELINE-RODADA-3.md`).

## Campos do deck

`src/mf/exportar_deck.py` grava os JSON de `deck/public/dados/`. Dois campos mudaram na rodada 2 da revisão:

| Campo | Coluna da base | Por quê |
|---|---|---|
| `dep` | `dep_transf`, com 8 casas decimais | Com 4 casas o componente classificava depois de arredondar, e a contagem de municípios acima de um corte errava de 1 a 2 em 13 combinações de grupo e corte (28 contando o seletor de tamanho). O corte de 80% não mudava |
| `rb` | `base`, a receita-base em reais | É o peso da composição por faixa. Antes o peso era a receita por habitante, arredondada ao real, vezes a população do Censo; o erro chegava a 0,03 ponto em São Paulo e Maranhão e a 0,15 entre as regiões |

O valor por habitante usa a população estimada do ano (campo `pop24`); o Censo 2022 define a faixa de tamanho.
O arredondamento fica para a tela.

## Limites que já se conhecem

- A DCA é declarada pela prefeitura. Convênio e emenda são classificados de modo desigual: a conta própria da
  emenda Pix registra 68% do valor pago em SP e 24% no MA, onde o dinheiro aparece em "outras transferências da
  União" (`revisao/claude/emendas-voluntarias.md`). E cerca de dois terços da emenda paga a prefeituras e fundos
  municipais vão para o fundo municipal de saúde (60% nos municípios de até 20 mil habitantes) e entram na conta
  do SUS. Por isso a emenda é medida só pelo Portal da Transparência.
- O custo da máquina pela função 01 mais a 04 não é comparável entre estados. Em São Paulo quase toda a
  administração geral está na função 04; fora de São Paulo, a administração da saúde e da educação é lançada
  dentro dessas funções (subfunção 122), e a medida vira um piso. Somar a subfunção 122 de todas as funções dá
  um teto, que pode carregar folha de saúde e de ensino. No Maranhão o teto é 59% maior que o piso; em São
  Paulo, igual.
- A relação entre custo da máquina e população é curva; uma elasticidade só não a resume.
- Receitas de uma vez só ficam dentro das fatias: precatório do antigo FUNDEF em "outras transferências"
  (R$ 1,4 bilhão em 159 municípios, quase todos do Nordeste) e outorga de concessão de saneamento em "demais
  receitas próprias" (Alagoas e Rio).
- O imposto de renda retido na fonte conta como tributo próprio, como na contabilidade oficial. Sem ele a
  autonomia cai cerca de 2 pontos; os indicadores com e sem estão na base.
- Nas comparações entre regiões os municípios de um mesmo estado se parecem e são só 13 estados: vale o maior
  entre o valor-p robusto e o agrupado por estado.
- A cota-parte do ICMS mistura devolução (valor adicionado, 74% em SP e 65% no MA) com redistribuição. Sem o
  índice de participação por componente não dá para separar as duas partes município a município.
- 2024 foi ano de eleição municipal. Com a média de 2023 a 2025, no painel de 3.261 municípios utilizáveis nos
  três anos, o retrato entre as regiões não muda: a dependência a tamanho igual vai de 6,7 para 7,1 pontos, o
  FPM como maior fatia fica em 65% no Sudeste e 47% no Nordeste, e a verba negociada e o custo da máquina ficam
  iguais (`revisao/claude/apoio/r3_trienio_13_estados.py`; `docs/ACHADOS.md` 11.8 e 15.2). O investimento é a
  exceção: no Nordeste, 2024 é o pico dos três anos. Os alertas de FPM e de FUNDEB só existem para 2024. No
  intervalo agrupado por estado do triênio usa-se t com 12 graus de liberdade.
- Convênio entra em pacote, num ano sim e noutro não. A mediana da média de três anos fica acima da mediana de
  cada ano e não serve para dizer que um ano foi fraco ou forte.
- `rec_corrente_liq` e `poupanca_corrente` contavam, até 06/10/2026, a transferência de capital de instituições
  privadas (R$ 3,346 bilhões em 107 municípios). Foi corrigido; nenhum achado usava as duas colunas.
- `docs/pesquisa/apoio/cem_confronto.py` e `revisao/claude/apoio/dm_3.py` somam as duas categorias de convênio
  de capital pelo nome antigo. Se forem rodados de novo sem ajuste, perdem os R$ 435 milhões que mudaram de
  categoria.
- Consórcios intermunicipais e gasto do estado feito direto no município não aparecem nas contas da prefeitura.
- É o universo dos municípios, não uma amostra: o valor-p pesa menos que o tamanho do efeito.

## Série longa

A evolução de 2000 a 2025 vem do IPEADATA, que publica as séries municipais da STN com todos os municípios numa
chamada. São os mesmos totais brutos das contas anuais: em 2024 a razão entre as duas fontes é 1,00000 na
mediana em sete séries. Por serem brutos (sem dedução do FUNDEB e sem tirar a previdência própria), os níveis
ficam alguns pontos acima dos da base principal; a série serve para tendência.

- Fica fora o par município-ano com transferência zerada ou abaixo de 5% da receita corrente (declaração
  incompleta, concentrada no Piauí e no Maranhão de 2013 a 2017) e o ano de 2008 (cobertura do Nordeste abaixo
  de 85%).
- As comparações começam em 2002: até 2001 o imposto de renda retido na fonte entrava como transferência e a
  função Administração tinha outra classificação.
- O grupo de tamanho usa a população de 2022 em todos os anos. Com a de 2010 a diferença máxima é de 0,4 ponto.

## Figuras

Cores da paleta validada pela rotina `validate_palette.js` (separação para daltonismo e contraste): a cor segue
a fatia em todas as figuras; laranja é São Paulo e Sudeste, violeta é Maranhão e Nordeste. No mapa da maior
fatia os royalties levam hachura, porque o par vermelho e verde-água fica fraco para quem não distingue as
duas cores. Caixas: metade central, mediana, hastes até a cerca de Tukey e pontos fora, com a contagem.

## Como refazer (PowerShell)

```powershell
$ErrorActionPreference = 'Stop'
$py = 'C:\dev\municipios-fiscal\.venv\Scripts\python.exe'
& $py C:\dev\municipios-fiscal\src\mf\baixar_ibge.py
& $py -u C:\dev\municipios-fiscal\src\mf\baixar_fila.py          # horas; pode parar e retomar
& $py C:\dev\municipios-fiscal\src\mf\extras.py
& $py C:\dev\municipios-fiscal\src\mf\montar_base.py 2022 2023 2024 2025
& $py C:\dev\municipios-fiscal\src\mf\relatorio.py 2024
& $py C:\dev\municipios-fiscal\src\mf\testes.py 2024
& $py C:\dev\municipios-fiscal\src\mf\figuras.py 2024 par SP MA
& $py C:\dev\municipios-fiscal\src\mf\figuras.py 2024 regioes
& $py C:\dev\municipios-fiscal\src\mf\ipeadata.py                 # série longa; precisa de dados\bruto\ipeadata
& $py C:\dev\municipios-fiscal\src\mf\testes_tempo.py             # acrescenta a família G a docs\TESTES.md; rodar depois de testes.py
& $py C:\dev\municipios-fiscal\src\mf\figuras_tempo.py longo
& $py C:\dev\municipios-fiscal\src\mf\figuras_tempo.py ifgf
& $py C:\dev\municipios-fiscal\src\mf\painel.py 2022 2023 2024 2025
& $py C:\dev\municipios-fiscal\src\mf\figuras_tempo.py dca
& $py C:\dev\municipios-fiscal\src\mf\exportar_deck.py
& $py C:\dev\municipios-fiscal\revisao\claude\apoio\r1_numeros_extras.py   # triênio, cortes e outras contas citadas em ACHADOS
& $py C:\dev\municipios-fiscal\revisao\claude\apoio\r3_trienio_13_estados.py   # triênio dos 13 estados (ACHADOS 15.2)
& $py C:\dev\municipios-fiscal\revisao\claude\apoio\r3_territorio.py           # área e população por tamanho (docs\tabelas\territorio_por_tamanho_2022.csv)
& $py C:\dev\municipios-fiscal\revisao\claude\apoio\r3_numeros_slides_novos.py # pizza média e acumulado de população (docs\tabelas)
& $py C:\dev\municipios-fiscal\revisao\claude\apoio\r3_fnp_definicao.py        # a conta da FNP refeita com a série do IPEADATA (ACHADOS 15.4)
& $py C:\dev\municipios-fiscal\docs\pesquisa\apoio\glossario_tendencias.py     # números do glossário das oito fontes de receita
```

A base de 2025 é montada antes das outras, porque é o denominador de `emenda_2025_sobre_base_2025`.
`r1_numeros_extras.py` filtrava mal o estado na conta do triênio de São Paulo e Maranhão: só dava certo
enquanto 2023 só tinha os dois estados. Foi corrigido em 06/10/2026. O relatório da execução da rodada 2 está
em `revisao/claude/r3/PIPELINE-RODADA-3.md`.
