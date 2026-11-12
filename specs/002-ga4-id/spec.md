# Spec 002: medição com Google Analytics 4

Status: em revisão (branch `002-ga4-id`, PR #2 em rascunho). Trabalho de 2026-11-09.

## Contexto
O site tinha só o marcador `G-XXXXXXXXXX`, então nenhuma visita era medida.

## Dados da conta
- GA4: ID de medição `G-V0QZN9HMV8`, fluxo da Web 160305398621.
- Tag do Google `GTM-MNNHV7PD`, gerada pelo próprio GA4 (sem contêiner no Tag Manager). O contêiner já envia para `G-V0QZN9HMV8`, conferido no `gtm.js`.
- Google Ads da Broker DF: conta 538-138-4156, sob a MCC da Amplixa 167-076-0025. Em 09/11 estava **cancelada** (status CLOSED); precisa ser reativada ou trocada antes de qualquer campanha.

## Decisão
As 3 páginas carregam **só** a tag `GTM-MNNHV7PD`. Não somar o gtag `G-V0QZN9HMV8` direto, porque isso contaria cada visita duas vezes.

## Commits da branch
1. `ef0552b` troca o marcador pelo ID real.
2. `14d979c` adiciona a tag e o GA4 em todas as páginas.
3. `e435224` deixa só a tag do Google, sem duplicar.

## Pendências
- Merge do PR #2, com aprovação. A branch foi criada antes da troca do WhatsApp (spec 003): conferir que o número antigo não volta.
- Depois do merge: confirmar visitas em tempo real no GA4.
