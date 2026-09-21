# Dez Orações

Uma declaração em dez poemas, dentro de um computador de mentira.
A tela inicial imita uma área de trabalho: toque duas vezes em `para_julia.exe`
e o jogo abre. Feito pra abrir no celular.

## Arquivos

| arquivo | o que é |
|---|---|
| `index.html` | o jogo inteiro — HTML, CSS e JavaScript num arquivo só |
| `wallpaper.webp` | o papel de parede da área de trabalho |
| `musica.mp3` | *(opcional)* trilha sonora — veja abaixo |

## Colocar uma música

Coloque um arquivo chamado `musica.mp3` nesta mesma pasta e ele toca em loop,
em fade, assim que o jogo começa. O botão ♪ no canto superior liga e desliga.

Se o arquivo não existir, o jogo toca uma valsa em 6/8 sintetizada na hora pelo
próprio navegador — nenhum download, nenhuma dependência externa.

Para usar outro nome ou formato (`.m4a`, `.ogg`), mude a constante `MUSICA`
no começo do `<script>`, dentro do `index.html`.

## Mudar o nome

No começo do `<script>`, dentro do `index.html`:

```js
let NOME = "Julia";     // o nome dela
let DE   = "Mateus";    // quem assina
```

Dá pra trocar pela URL também, sem mexer no código:
`.../index.html?nome=Julia&de=Mateus`

## Mudar os poemas

Os dez níveis ficam na lista `NIVEIS`, também no `<script>`. Cada um tem:

```js
{
  mec:"luzes",        // luzes | segurar | contar | medos | arrastar
  rotulo:"...",       // a instrução na tela
  titulo:"...",
  verso:"...",        // o versículo
  poema:`...`         // linhas em branco separam as estrofes
}
```

## Publicar

O site é estático: basta servir esta pasta. No GitHub Pages, ative em
**Settings → Pages → Branch: main / (root)**.

Para testar no computador antes, abra o `index.html` direto no navegador —
funciona sem servidor.
