# Marcador de Pontos (app web)

Marcador de pontos por rodada com ranking ao vivo. Cada rodada você digita os pontos tomados por jogador, com ou sem sinal negativo. Quem chega à pontuação limite sai do jogo, e o jogo segue até sobrar um. Funciona sem internet depois da primeira abertura e se instala na tela inicial do iPhone como um app.

## Como funciona

1. **Início:** adicione os jogadores e defina a pontuação limite. Toque em Iniciar jogo.
2. **Durante:** digite os pontos tomados por cada jogador na rodada e toque em Finalizar e ir para a próxima. Para pontos negativos, toque no botão **±** dentro do campo antes de digitar o número.
3. **Ranking (aba lateral):** toque na aba "Ranking" na borda direita para abrir. Ele atualiza enquanto você digita. Em telas largas (iPad, computador) ele fica fixo ao lado.

No ranking, quem tem menos pontos é o primeiro. As cores vão do verde (1º) ao vermelho (último) e o eliminado fica cinza. Jogadores empatados dividem a mesma posição.

## Arquivos

- `index.html`: o app inteiro.
- `manifest.webmanifest`: nome, cores e ícones do app.
- `sw.js`: guarda o app no aparelho para abrir offline.
- `icons/`: ícones do app.
- `splash/`: telas de abertura para iPhone, nos modos claro e escuro.

## Publicar no GitHub Pages

1. No GitHub, crie um repositório novo (por exemplo `marcador`).
2. Envie todos os arquivos desta pasta, mantendo as pastas `icons` e `splash`. O `index.html` fica na raiz.
3. Em Settings > Pages, escolha a branch `main` e a pasta `/ (root)`.
4. Aguarde um ou dois minutos. O endereço será parecido com `https://SEU-USUARIO.github.io/marcador/`.

Os caminhos são relativos, então funciona na raiz do site e em subpastas.

## Instalar no iPhone

1. Abra o endereço no **Safari**.
2. Toque em **Compartilhar** (quadrado com seta para cima).
3. Toque em **Adicionar à Tela de Início** e depois em **Adicionar**.

Abra o app sempre pelo ícone da tela inicial. O jogo em andamento fica salvo no próprio aparelho, e o ícone guarda os dados separados do Safari. Use um único celular como marcador.

No Android, abra no Chrome e toque em Instalar app.

## Atualizar o app

Depois de mudar qualquer arquivo, aumente o número em `VERSION` no começo de `sw.js` (por exemplo, de `marcador-v2` para `marcador-v3`). Assim os aparelhos baixam a versão nova na próxima abertura. Se o iPhone mostrar um ícone antigo, remova o app da tela inicial e adicione de novo.
