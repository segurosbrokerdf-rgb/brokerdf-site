# Plano de indexação e acompanhamento

Baseado no que já foi feito na Amplixa. Executar depois do merge, pois as páginas novas precisam estar no ar.

## Dia do merge
1. **Google Search Console:** criar uma propriedade de domínio para `brokerdf.com.br`, verificada por registro TXT no DNS. Ela cobre `www` e a versão sem `www`.
2. **Sitemap:** enviar `https://www.brokerdf.com.br/sitemap.xml` em *Sitemaps*.
3. **Pedir indexação:** em *Inspeção de URL*, testar e solicitar a home e as duas páginas novas.
4. **Bing Webmaster Tools:** importar a propriedade do Search Console e conferir o sitemap.
5. **Perfil da Empresa no Google:** criar ou revisar, com nome, endereço e telefone iguais aos do site. Depois da verificação, ligar o perfil no schema do site (`sameAs` e `hasMap`).
6. **GA4:** feito em 09/11/2026 (branch `002-ga4-id`). ID de medição `G-V0QZN9HMV8`, fluxo da Web 160305398621, em todas as páginas. Google Tag Manager `GTM-MNNHV7PD` (código oficial, com noscript) também em todas as páginas. Se o contêiner do GTM ganhar uma tag do GA4 com o mesmo ID, remover o gtag direto para não contar visitas em dobro. Falta: vincular ao Google Ads da Broker DF (conta sob a MCC da Amplixa 167-076-0025) e marcar `generate_lead` como evento principal depois do primeiro disparo.

## Primeiras semanas
- Conferir em *Páginas* se as 3 URLs foram indexadas e se a versão canônica escolhida pelo Google é a `www`. O prazo pode variar de dias a semanas.
- Registrar a posição de partida para: plano de saúde Brasília, corretora de plano de saúde DF, seguro de vida Brasília, corretora de seguro de vida DF.

## Rotina
- **Semanal:** cliques, impressões e posição no Search Console, além do PageSpeed. A nota do PageSpeed oscila: não reagir a uma medição isolada.
- **Trimestral:** repetir a pesquisa de concorrentes com busca real no DF.

## Próximos passos, conforme os dados
- Páginas por operadora e por região, que os concorrentes já usam.
- Monitorar a presença em respostas de IA. O `robots.txt` atual já não bloqueia esses rastreadores.
