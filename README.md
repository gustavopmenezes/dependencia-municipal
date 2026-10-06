# De onde vem o dinheiro das prefeituras

**Sudeste × Nordeste · São Paulo × Maranhão.** Contas municipais de 2024, série de 2002 a 2025.

Autor: Gustavo Menezes (gustavopmenezes@usp.br).

- Deck interativo: https://gustavopmenezes.github.io/dependencia-municipal/
- E-book (PDF): https://gustavopmenezes.github.io/dependencia-municipal/relatorio.pdf

## O que é

Um estudo que pergunta se a proporção entre as fontes de receita dos municípios difere muito entre regiões, e se
o interior de São Paulo depende de receita externa tanto quanto o Maranhão. Usa as contas anuais de 2024 dos
municípios dos 13 estados do Nordeste e do Sudeste (Tesouro Nacional, SICONFI), a série municipal de 2002 a 2025
(IPEADATA), o Censo 2022 (IBGE) e as emendas federais pagas em 2025 (Portal da Transparência).

No deck, todo mapa e todo gráfico responde a clique: clicar num município abre a ficha dele, clicar numa classe
da legenda lista os municípios da classe, e o botão "ver tabela" mostra os dados por trás do desenho e baixa em
CSV.

## O que há neste repositório

| Caminho | Conteúdo |
|---|---|
| `index.html`, `assets/`, `dados/` | o site do deck, já construído (Slidev) |
| `relatorio.pdf` | o e-book |
| `docs/RELATORIO.md`, `docs/relatorio/figuras/` | o texto do e-book em Markdown, com as figuras |
| `docs/ACHADOS.md` | os achados numerados, com a lista do que cada conferência derrubou |
| `docs/METODO.md`, `docs/HIPOTESES.md`, `docs/TESTES.md`, `docs/NUMEROS.md` | método, hipóteses escritas antes dos testes, resultados e tabelas |
| `docs/REFERENCIAS.md` | todas as fontes, em ABNT, com a lista das que não foram conferidas |
| `docs/NOTA-DE-METODO.md` | quem fez o quê: o autor e os modelos de linguagem |
| `docs/nt23-cem/` | cópia da Nota Técnica 23 do Centro de Estudos da Metrópole (Peres, Marques e Armani, 2025), que o deck mostra página a página. O original está em https://centrodametropole.fflch.usp.br/sites/centrodametropole.fflch.usp.br/files/inline-files/nt23.pdf |

O código e a base por município ficam com o autor. Os vídeos citados não são copiados para cá: o deck os mostra a
partir do endereço original.

## Como citar

MENEZES, Gustavo Paixão. **De onde vem o dinheiro das prefeituras**: São Paulo e Maranhão, Sudeste e Nordeste nas
contas municipais de 2024. São Carlos, 2026. Disponível em:
https://gustavopmenezes.github.io/dependencia-municipal/relatorio.pdf. Acesso em: 6 out. 2026.

## Limites

Contas declaradas pelas próprias prefeituras; retrato de um ano, conferido contra a média de 2023 a 2025; só
Nordeste e Sudeste; emenda federal paga a prefeituras e fundos municipais, sem a emenda estadual. Nenhum
especialista em finanças municipais leu o trabalho. O estudo descreve e não recomenda política pública. O método e
os limites estão em `docs/METODO.md`.
