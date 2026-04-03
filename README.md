# LINKr

LINKr é uma página simples para montar uma “link page” a partir de parâmetros na URL.

## Como usar

A aplicação lê os parâmetros da query string (parte após `?`) e renderiza os links na tela.

Exemplo:

```text
https://wllr9505.github.io/linkr/?l=gh/WLLR9505,ig/wllr9505
```

## Parâmetros de URL

| Parâmetro | Tipo | Obrigatório | Tipo de destino | Descrição | Exemplo |
| --- | --- | --- | --- | --- | --- |
| `l` | string (lista separada por vírgula) | Não | Misto: principalmente páginas de perfil, mas também destinos gerais (ex.: convites, páginas de empresa, artigos, páginas arquivadas) | Lista de links no formato `prefixo/caminho`. Cada item vira um link na página. | `?l=gh/WLLR9505,ig/wllr9505` |

## Prefixos suportados em `l`

Use os prefixos abaixo antes da barra (`/`) para montar automaticamente o domínio:

| Prefixo | Base gerada | Tipo de página de destino |
| --- | --- | --- |
| `aws` | `aws.amazon.com/` | Página geral |
| `db` | `dropbox.com/` | Arquivo/pasta |
| `dc` | `discord.gg/` | Convite de servidor |
| `fb` | `facebook.com/` | Página/perfil |
| `gd` | `drive.google.com/` | Arquivo/pasta |
| `gh` | `github.com/` | Perfil/repositório |
| `gl` | `gitlab.com/` | Perfil/repositório |
| `ig` | `instagram.com/` | Perfil |
| `kck` | `kick.com/` | Perfil/canal |
| `li` | `linkedin.com/in/` | Perfil |
| `ln` | `linkedin.com/company/` | Página de empresa |
| `pn` | `pinterest.com/` | Perfil/pasta |
| `rd` | `reddit.com/` | Perfil/comunidade/post |
| `sc` | `soundcloud.com/` | Perfil/faixa |
| `sp` | `spotify.com/` | Perfil/faixa/playlist |
| `stm` | `steamcommunity.com/id/` | Perfil |
| `tg` | `t.me/` | Perfil/canal/grupo |
| `tt` | `tiktok.com/@` | Perfil |
| `ttv` | `twitch.tv/` | Canal |
| `tw` | `twitter.com/` | Perfil/post |
| `vsc` | `vsco.co/` | Perfil |
| `wb` | `web.archive.org/web/` | Página arquivada |
| `wkp` | `wikipedia.org/wiki/` | Artigo |
| `wp` | `wordpress.com/` | Site/página |
| `yt` | `youtube.com/@` | Canal |

Se o prefixo não existir na lista, o valor é tratado como URL direta após `https://`.
