# Spec 003: troca do número de WhatsApp

Status: publicada em 2026-11-09 (PR #3, merge `724e24a`).

## Pedido
Em 2026-11-09 o Bruno pediu trocar o WhatsApp para **(61) 99983-5948**, no lugar de (61) 98427-5522, e publicar.

## O que mudou
Na home e nas páginas de plano de saúde e seguro de vida:
- links `wa.me/5561999835948` (botões, cards e envio do formulário);
- número exibido no rodapé e na seção de contato;
- `telephone` dos dados estruturados da home;
- exemplo do campo de telefone do formulário.

## Verificação
Depois do merge, as 3 páginas publicadas foram baixadas: o número novo aparece em todas, e o antigo em nenhuma.

## Pendência
Atualizar o número no Perfil da Empresa no Google, se ele usar o WhatsApp.
