# Spec 002: medição com Google Analytics 4

Status: publicada em 2026-11-12 (PR #2, merge `f809e76`). Trabalho de 2026-11-09.

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

## Incidente: GA4 sem dados por 3 dias
Em 2026-11-12 o GA4 avisou "A coleta de dados não está ativa no seu site". Causa: o PR #2 ficou em rascunho de 09/11 a 12/11 e o site no ar ainda tinha o marcador `G-XXXXXXXXXX`. Lição: tag pronta só mede depois do merge; conferir o site publicado, não a branch.

## Verificação após o merge (2026-11-12)
- As 3 páginas publicadas têm a tag `GTM-MNNHV7PD` logo após o `<head>`, igual à fornecida pelo GA4.
- Nenhuma página tem mais `G-XXXXXXXXXX` nem um segundo gtag.
- O WhatsApp (61) 99983-5948 continua em todas as páginas (sem regressão da spec 003).
- `gtm.js?id=GTM-MNNHV7PD` responde 200.

## Pendências
- Bruno: usar **Testar** nas instruções da tag e conferir **Relatórios → Tempo real**. O aviso amarelo pode levar até 48 horas para sumir.
