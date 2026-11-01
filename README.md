# Radar de Preços

Menor preço de qualquer produto, com histórico, previsão e alerta no celular: https://talles2026.github.io/radar-precos/

- Digite o produto; o tipo é identificado sozinho. Veículos: OLX, Mercado Livre, Facebook Marketplace e Google. Demais: Mercado Livre, Shopee, Amazon, AliExpress e Google.
- Preços lidos direto na Amazon, AliExpress e OLX, e pelos comparadores Bing Shopping e Buscapé (onde aparece o Mercado Livre). Shopee, Google, Facebook e o Mercado Livre direto bloqueiam leitura automática: o app mostra o atalho da busca já ordenada pelo menor preço.
- Atualiza ao abrir e a cada 30 minutos. App instalável (botão Instalar).
- Servidor: função `precos` no Supabase (projeto radar-clima), código em `supabase/functions/precos/`; tabelas `precos_produtos`, `precos_hist`, `precos_inscricoes`; agendamento `precos-atualizar` (pg_cron).
