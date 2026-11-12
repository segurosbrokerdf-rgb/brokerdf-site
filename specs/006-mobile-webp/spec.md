# Spec 006: largura no celular, contraste e foto em WebP

Status: em revisão (branch `006-mobile-webp`, PR #6). Trabalho de 2026-11-12.

## Problemas
1. No celular (390 px), a home tinha 693 px de largura e arrastava para o lado. Causas:
   - os cards Pessoa Física e Empresarial (`#planos`) ficavam lado a lado, com estilo inline de duas colunas;
   - a seção de contato tinha textos sem quebra de linha (e-mail) e colunas sem `min-width: 0`.
2. O botão "Falar no WhatsApp" dos cards usava o estilo do topo azul (texto branco) e ficava quase invisível no fundo claro, no celular e no computador.
3. `ceo-brokerdf.jpg` (36 KB, 537x800) era exibida com 140 px.

## Mudanças em `index.html`
- Classe `planos-grid` nos cards; no celular, uma coluna e menos espaço lateral.
- Contato: colunas com `minmax(0, 1fr)`, `min-width: 0` e quebra de textos longos.
- Botão secundário dos cards em azul com contorno.
- Foto via `<picture>`: `ceo-brokerdf.webp` (280x417, 6,5 KB, nitidez para telas 2x) com o JPG como reserva, e `width`/`height` declarados.
- Horário de atendimento já exibido na página (segunda a sexta, 9h às 18h) incluído nos dados estruturados.

## Verificação local (`npx serve` + Chrome)
- Largura da página no celular: 390 px (antes 693 px), sem nenhum elemento passando da tela.
- O navegador carrega a versão WebP.
- Cards conferidos por captura de tela no celular e no computador.
- JSON-LD válido.

## Decisão registrada
Registro SUSEP não será incluído no site (Bruno, 2026-11-12).
