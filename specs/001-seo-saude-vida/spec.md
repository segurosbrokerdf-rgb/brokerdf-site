# Spec 001: SEO para plano de saúde e seguro de vida no DF

Status: em revisão (branch `001-seo-saude-vida`). Criada em 2026-11-03.

## Objetivo
Melhorar a posição do site no Google em buscas de plano de saúde e seguro de vida no Distrito Federal.

## Limite do benchmark
A ferramenta de busca usada roda nos EUA e não é o Google Brasil. Os concorrentes abaixo são **uma aproximação**, não o top 3 confirmado do Google no DF. Falta conferir em aba anônima, a partir do DF. As lacunas se repetem em todos, então as ações tendem a valer mesmo que a lista mude. A Unimed DF ficou fora por ser operadora, não corretora. Medlife e SD Corretora recusaram a coleta automática (HTTP 406).

## Benchmark (páginas coletadas em 2026-11-03)
| Site | Foco | Title | H1 | Dados estruturados | Palavras | FAQ | Páginas dedicadas |
|---|---|---|---|---|---:|---|---|
| corretorals.com.br | Saúde | Planos de Saúde Brasília 2026 + benefício | Institucional | InsuranceAgency, FAQPage, Service, OfferCatalog, AggregateRating | 917 | Sim | Por operadora e por intenção |
| healthcarebrasilia.com | Saúde | Plano De Saúde + modalidades | Plano De Saúde DF | Article, WebPage, PostalAddress | 2510 | Não | Por operadora, tabelas |
| seg10.com.br (página de vida) | Vida | Seguro de Vida em Brasília - Distrito Federal | Igual ao title | LocalBusiness | 2009 | H2 em forma de pergunta | Por produto + cidade |
| starcorretoradeseguros.com.br (página de vida) | Vida | Seguro de Vida em Brasília (DF) | Igual ao title | Article, BreadcrumbList, Organization | 826 | Não | Por produto e por público |
| **brokerdf.com.br (antes)** | Ambos | Plano de Saúde + marca, sem local | Sem local e sem vida | InsuranceAgency | 1048 | Não | **Nenhuma** |

## Resultado real do Google (print do Bruno, 2026-11-03)
Busca: "corretora plano de saúde Brasília". O Broker DF não aparece na parte visível do print.

| Posição | Quem | Sinais visíveis |
|---|---|---|
| Mapa 1 | Corretora de Planos de Saúde em Brasília | 5,0 com 427 avaliações |
| Mapa 2 | LS Corretora Planos de Saúde | 5,0 com 251 avaliações |
| Mapa 3 | Vilma Lins Planos de saúde | 5,0 com 69 avaliações |
| Orgânico 1 | Star Corretora (`/planos-de-saude-...`) | Página dedicada, title "Planos de Saúde Brasília (DF)" |
| Orgânico 2 | Medlife Seguros (home) | Title "Planos de Saúde em Brasília-DF" |

O mapa vem antes dos resultados orgânicos, e as avaliações se destacam nele. O Perfil da Empresa e a coleta de avaliações reais passam a ser prioridade. A busca de seguro de vida ainda não foi conferida.

## Lacunas encontradas
1. Uma única página tenta atender todas as buscas.
2. Title, description e H1 não citam Brasília/DF nem seguro de vida.
3. Canonical, `og:url` e schema apontam para `brokerdf.com.br`, que redireciona (301) para `www`.
4. `robots.txt` e `sitemap.xml` retornam 404.
5. Schema com `areaServed: Brasil` e sem serviços.
6. `ceo-brokerdf.jpg` com 9,7 MB.
7. `CENAME` é uma cópia sem uso de `CNAME`.
8. Links de serviços do rodapé só apontam para âncoras da home.

## Requisitos
- RF1: página própria para plano de saúde no DF e outra para seguro de vida no DF.
- RF2: home com title, description, H1 e schema orientados a saúde, vida e DF.
- RF3: FAQ visível para o leitor, sem schema FAQPage: o Google encerrou esse resultado em 07/05/2026 (aprendizado da Amplixa).
- RF4: `robots.txt`, `sitemap.xml` e URL canônica única em `www`.
- RF5: imagem da CEO abaixo de 300 KB.
- RF6: especificações fora do site publicado.
- RF7: site indexado no Google e no Bing, conforme `indexacao.md`.

## Regras de conteúdo
- Reproduzir a estrutura dos concorrentes, nunca o texto.
- Não inventar preços, avaliações, número de clientes, seguradoras ou registros.
- Não usar AggregateRating sem avaliações reais.

## Fora do escopo (depende do Bruno ou de acessos)
- Perfil da Empresa no Google: provavelmente o maior fator nas buscas locais.
- ID real do GA4 (hoje é o marcador `G-XXXXXXXXXX`, sem medição) e Search Console.
- Número de registro SUSEP, seguradoras de vida parceiras e horário de atendimento.
- Definir se o site atende só o DF ou também outras regiões.
