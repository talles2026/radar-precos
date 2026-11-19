# Radar de Preços

Menor preço de qualquer produto, com histórico, previsão e alerta no celular: https://talles2026.github.io/radar-precos/

- Digite o produto; o tipo é identificado sozinho. Veículos: OLX, Mercado Livre, Facebook Marketplace e Google. Demais: Mercado Livre, Shopee, Amazon, AliExpress e Google.
- Preços lidos direto na Amazon, AliExpress e OLX, e pelos comparadores Bing Shopping e Buscapé (onde aparece o Mercado Livre). Shopee, Google, Facebook e o Mercado Livre direto bloqueiam leitura automática: o app mostra o atalho da busca já ordenada pelo menor preço.
- Veículos: o texto da busca vira filtro. Ex.: "Hilux 2002 a 2005 cabine simples 4x4" procura "hilux" na OLX (e cada ano da faixa, até 4 buscas), aceita só anúncios dentro da faixa de ano, recusa os que dizem cabine dupla ou 4x2 e marca "confira" quando o anúncio não informa cabine/tração. Os atalhos das lojas já levam os filtros (Facebook com ano mínimo/máximo, Google com a faixa de ano).
- Tela: busca no topo, produtos ativos logo abaixo (toque para ver), e o painel do produto com o menor preço e o preço em cada loja; histórico, previsão e alerta ficam recolhidos.
- Aviso no celular sempre que o menor preço de um produto ativo baixar (1% ou mais em relação à busca anterior; o mesmo preço não repete em 24 h) e quando chegar no alvo.
- Atualiza ao abrir e a cada 30 minutos. App instalável (botão Instalar).
- Servidor: função `precos` no Supabase (projeto radar-clima), código em `supabase/functions/precos/`; tabelas `precos_produtos`, `precos_hist`, `precos_inscricoes`; agendamento `precos-atualizar` (pg_cron).
