# Merca Livre

Um simulador casual de comércio em navegador. Compre lotes no Dragão Express, anuncie produtos em estoque no Merca Livre e invista no Banco Capivara. As marcas são paródias fictícias.

## Rodar localmente

Requer Node.js 20.19+ ou 22.12+.

```bash
npm install
npm run dev
```

Para gerar os arquivos estáticos: `npm run build`.

## Como jogar

1. A categoria **Achadinhos** começa liberada, com cinco itens de até R$ 15 de custo. A compra reserva espaço no depósito antes da entrega.
2. Cada categoria tem seu prazo base de frete: 1, 2, 3, 5, 8 e 12 minutos. Logística reduz o prazo e o custo dos próximos lotes, com entrega mínima de um minuto.
3. Quando as unidades chegarem, publique o anúncio no **Merca Livre**. Só há anúncio novo com estoque. Ao esgotar, o anúncio para de receber visitas até a reposição.
4. A cada minuto, o jogo sorteia visitas, compradores e pedidos. Alguns clientes compram várias unidades ou produtos diferentes. Marketing aumenta visitas; conversão aumenta compradores; retenção aumenta o tamanho dos pedidos.
5. Desbloqueie a categoria seguinte após vender a quantidade exigida na categoria anterior **e** pagar a taxa. O depósito começa com 20 espaços e pode ser ampliado. Veículos usam vagas em um pátio separado.
6. Na aba **Relatórios**, veja o funil de cada ciclo, produtos, pedidos com nomes fictícios, receita, taxas e totais acumulados. Os 120 ciclos recentes têm detalhes; os totais continuam acumulados.

## Salvamento

A partida fica no `localStorage` deste navegador. Não há servidor, contas ou sincronização entre dispositivos. Ao voltar à página, o jogo simula os ciclos perdidos; após mais de sete dias, processa os últimos sete dias para preservar o desempenho. Partidas da versão anterior são migradas preservando dinheiro, estoque e anúncios; o depósito antigo mantém sua capacidade para não invalidar os lotes existentes. Os preços e probabilidades são parâmetros de jogo sujeitos a balanceamento. Não há transações com dinheiro real.
