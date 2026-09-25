# Merca Livre

Um simulador casual de comércio em navegador. Pesquise produtos no Dragão Express, compre estoque, publique anúncios no Merca Livre e acompanhe o caixa no Banco Capivara. As marcas são paródias fictícias.

## Rodar localmente

Requer Node.js 20.19+ ou 22.12+.

```bash
npm install
npm run dev
```

Abra o endereço indicado pelo Vite. Para gerar uma versão estática: `npm run build`.

## Como jogar

1. Compre um lote no **Dragão Express**. Ele chega após 5 a 7 minutos reais, conforme o produto. O upgrade de frete reduz o prazo de compras futuras.
2. Quando houver unidades em estoque, publique o produto no **Merca Livre** e defina o preço. Produtos sem estoque não podem ser anunciados; anúncios esgotados aguardam reposição.
3. A cada minuto, o jogo sorteia visitantes para cada anúncio com estoque. Parte deles compra; alguns levam mais de uma unidade. Preço, concorrência e reputação influenciam as chances.
4. No **Banco Capivara**, invista em marketing (visitas), conversão (compradores), retenção (unidades por comprador) e frete (entrega).

O jogo simula os ciclos perdidos quando você volta à aba, sem precisar deixar o navegador aberto. A partida fica no `localStorage` deste navegador: não há servidor, contas ou sincronização entre dispositivos. Ao reabrir após mais de sete dias, o jogo processa até sete dias de ciclos para manter o desempenho. A versão anterior da partida é migrada automaticamente; anúncios antigos sem estoque são pausados. Não há compras com dinheiro real.
