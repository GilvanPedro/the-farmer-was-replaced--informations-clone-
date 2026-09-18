# The Farmer Was Replaced — Documentação (recriada)

Este repositório é uma recriação, em HTML/CSS/JS puro, do manual in-game do jogo **The Farmer Was Replaced** (Metaroot). Todo o conteúdo textual — títulos, explicações, exemplos de código e valores — foi retirado diretamente das telas de documentação existentes dentro do próprio jogo. Nada aqui foi inventado: o trabalho foi reconstruir a interface e a navegação como um site estático de várias páginas, mantendo os links internos entre os tópicos exatamente como funcionam no jogo.

Como bônus, o projeto também inclui um terminal Python funcional com uma simulação simplificada da fazenda, para testar trechos de código fora do jogo.

## Aviso importante

Este é um projeto não oficial, feito por um fã, sem qualquer vínculo com a Metaroot ou com o desenvolvimento de *The Farmer Was Replaced*. Todo o conteúdo textual reproduzido aqui (nomes de funções, descrições, textos das páginas de Unlocks, Items, Entities etc.) pertence aos criadores originais do jogo — apenas a apresentação em formato de site estático é deste repositório. Se você ainda não jogou, considere conferir o jogo original.

Créditos do jogo (conforme a própria página de créditos in-game):

- Programação, Game Design e Arte: Timon Herzog
- Música e Efeitos Sonoros: Floris Demandt
- Publicado por Metaroot

## O que tem aqui

O site reproduz a estrutura de navegação do manual in-game, dividida nas mesmas seções:

- **General Info** — primeiros passos, editor externo, backups, output, stats e créditos.
- **Programming** — a referência completa de linguagem usada no jogo: variáveis, condicionais, laços, funções, escopos, listas, dicionários, tuplas, sets, operadores, comentários, imports e timing.
- **Unlocks** — a árvore de desabloqueios do jogo (Auto Unlock, Cactus, Carrots, Debug, Expand, Fertilizer, Hats, Mazes, Megafarm, Polyculture, Pumpkins, Senses, Speed, Sunflowers, Timing, Trees, Utilities, Watering, entre outros).
- **Built-in Functions** — a referência de cada função nativa do jogo (assinatura, retorno, custo em ticks e um exemplo), de `abs()` a `wait_for()`.
- **Items** — os recursos coletáveis (Hay, Wood, Carrot, Pumpkin, Cactus, Bone, Weird Substance, Gold, Water, Fertilizer, Power).
- **Entities** — as plantas e objetos que existem na fazenda (Apple, Bush, Cactus, Carrot, Dead Pumpkin, Dinosaur, Grass, Hedge, Pumpkin, Sunflower, Treasure, Tree).
- **Grounds** — os tipos de terreno (Grassland, Soil).

Cada palavra que no jogo aparecia como link sublinhado em verde vira, aqui, um link `<a>` de verdade para a página correspondente, permitindo navegar pelo manual exatamente como dentro do jogo.

## Terminal Python (bônus)

Além da documentação, o repositório inclui uma página de terminal (`terminal.html`) com:

- Um interpretador Python real rodando no navegador (via Pyodide), sem precisar instalar nada.
- Um ambiente simulado com as funções e constantes do jogo (`move`, `harvest`, `plant`, `till`, `can_harvest`, `Entities`, `Items`, `Grounds`, `North`/`East`/`South`/`West` etc.), para testar scripts fora do jogo.
- Uma visualização da fazenda ao vivo, ao lado do editor, desenhada com emojis e construída em TypeScript (compilado no próprio navegador), que anima cada ação do drone conforme o código roda.
- Suporte a laços contínuos (`while True`): quando o script não tem uma condição de parada, a simulação continua automaticamente em ciclos, preservando o estado da fazenda, até você clicar em "Parar".

Essa parte é uma simulação simplificada, feita para fins de estudo da sintaxe — não reproduz timers de crescimento, custos reais ou o balanceamento exato do jogo.

## Como usar

Não há build nem dependências para instalar. É um site estático.

1. Baixe ou clone o repositório.
2. Abra `index.html` no navegador — é a página geral, com o menu de todos os tópicos.
3. Navegue normalmente pelos links, como faria dentro do jogo.

Para hospedar no GitHub Pages, basta ativar o Pages apontando para a raiz do repositório (ou para a branch/pasta onde os arquivos `.html` estão) — nenhuma etapa de build é necessária.

## Estrutura

- Cada tópico do manual é um arquivo `.html` independente, nomeado a partir do próprio título da página (por exemplo, `for-loop.html`, `dictionaries.html`, `get-pos-x.html`).
- `index.html` é a página geral (Home), com a lista completa de tópicos.
- `terminal.html` é o terminal Python com a simulação visual da fazenda.
- Todas as páginas compartilham o mesmo visual (janela escura, barra de título com "Voltar" e "Página Geral") e usam apenas HTML, CSS e JavaScript — sem frameworks e sem etapa de compilação, exceto pelo TypeScript do painel de jogo do terminal, que é transpilado em tempo real no navegador.

## Licença e uso

O código deste site (HTML/CSS/JS/TS escritos para reconstruir a interface) pode ser usado livremente. O conteúdo textual do jogo reproduzido aqui pertence aos seus respectivos autores e é usado apenas com finalidade de referência e estudo.

## Creditos

Feito por Gilvan Pedro com o auxílio do Claude Ai
