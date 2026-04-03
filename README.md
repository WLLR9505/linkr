# LINKr

LINKr é uma página simples para montar uma “link page” a partir de parâmetros na URL.

## Como usar

A aplicação lê os parâmetros da query string (parte após `?`) e renderiza os links na tela.

Exemplo:

```text
https://wllr9505.github.io/linkr/?l=gh/WLLR9505,ig/wllr9505,yt/canal
```

## Parâmetros de URL

| Parâmetro | Tipo | Obrigatório | Descrição | Exemplo |
| --- | --- | --- | --- | --- |
| `l` | string (lista separada por vírgula) | Não | Lista de links no formato `prefixo/caminho`. Cada item vira um link na página. | `?l=gh/WLLR9505,ig/wllr9505` |

## Prefixos suportados em `l`

Use os prefixos abaixo antes da barra (`/`) para montar automaticamente o domínio:

| Prefixo | Base gerada |
| --- | --- |
| `aws` | `aws.amazon.com/` |
| `db` | `dropbox.com/` |
| `dc` | `discord.com/` |
| `fb` | `facebook.com/` |
| `gd` | `drive.google.com/` |
| `gh` | `github.com/` |
| `gl` | `gitlab.com/` |
| `ig` | `instagram.com/` |
| `kck` | `kick.com/` |
| `li` | `linkedin.com/in/` |
| `ln` | `linkedin.com/company/` |
| `pn` | `pinterest.com/` |
| `rd` | `reddit.com/` |
| `sc` | `soundcloud.com/` |
| `sp` | `spotify.com/` |
| `stm` | `steamcommunity.com/id/` |
| `tg` | `t.me/` |
| `tt` | `tiktok.com/@` |
| `ttv` | `twitch.tv/` |
| `tw` | `twitter.com/` |
| `vsc` | `vsco.co/` |
| `wb` | `web.archive.org/web/` |
| `wkp` | `wikipedia.org/wiki/` |
| `wp` | `wordpress.com/` |
| `yt` | `youtube.com/@` |

Se o prefixo não existir na lista, o valor é tratado como URL direta após `https://`.
