# Site Broker DF

Site estático de https://www.brokerdf.com.br/, hospedado no GitHub Pages a partir da branch `main`. O DNS fica no registro.br.

## Como trabalhar
- Cada mudança tem uma spec em `specs/NNN-nome/` e uma branch própria.
- A mudança vai para revisão em um Pull Request. O merge na `main` publica o site na hora, então só acontece com aprovação. Depois do merge, conferir o site publicado.
- Autor dos commits: `segurosbrokerdf-rgb <segurosbrokerdf@gmail.com>`.
- `specs/` e este README não são publicados (`_config.yml`).
- Teste local: `npx serve .` na raiz.

## Histórico
| Spec | Assunto | Situação |
|---|---|---|
| 001 | SEO para plano de saúde e seguro de vida, páginas dedicadas, robots, sitemap, plano de indexação | Publicada em 2026-11-03 (PR #1) |
| 002 | GA4 pela tag do Google `GTM-MNNHV7PD` (envia para `G-V0QZN9HMV8`) | Publicada em 2026-11-12 (PR #2) |
| 003 | WhatsApp trocado para (61) 99983-5948 | Publicada em 2026-11-09 (PR #3) |
| docs | README e specs 002/003 (PR #4); atualização após publicar o GA4 (PR #5) | Publicadas em 2026-11-12 |

## Pendências
- Confirmar visitas no Tempo real do GA4 (tag publicada em 2026-11-12).
- Corrigir a largura da home no celular.
- Converter `ceo-brokerdf.jpg` para WebP e reduzir o tamanho.
- Search Console: propriedade de domínio com TXT no registro.br, sitemap e pedido de indexação (`specs/001-seo-saude-vida/indexacao.md`).
- Perfil da Empresa no Google: confirmar se existe e atualizar o WhatsApp.
- Google Ads 538-138-4156 está cancelado: reativar ou trocar de conta.
- Seguradoras de vida parceiras, registro SUSEP e horário de atendimento.
- Bing Webmaster Tools, depois do Search Console.
