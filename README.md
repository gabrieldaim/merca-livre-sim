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

1. Escolha um produto em **Dragão Express** e compre um lote. A compra ocupa capacidade futura do depósito.
2. Publique o anúncio no **Merca Livre**, definindo preço e gasto diário em publicidade.
3. Avance os dias. As compras chegam depois de 2 ou 3 dias; vendas são calculadas com demanda variável, preço, concorrência, publicidade e reputação.
4. No **Banco Capivara**, invista para reduzir o intervalo entre avanços de 5 para 4, 3 e 2 minutos.

A partida é salva automaticamente no `localStorage` deste navegador. Não há contas nem sincronização. Os primeiros 5 minutos só começam depois do primeiro avanço. A demanda é uma estimativa; o resultado real varia a cada dia.

## Escopo desta versão

O jogo tem oito produtos, taxas do marketplace, defeitos ocasionais na chegada, vendas perdidas por falta de estoque, crédito de recuperação e extrato. Os números são parâmetros iniciais para balanceamento, não uma simulação econômica real. Não há compras com dinheiro real.
