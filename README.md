# Pizzaria Controle

Sistema de controle operacional para pizzarias — aplicação web standalone (HTML/CSS/JS puro, sem dependências de build).

## Como usar

Abra o arquivo `index.html` diretamente no navegador. Nenhuma instalação necessária.

## Funcionalidades

### Dashboard
- KPIs do dia: total de vendas, lucro, quantidade de pizzas e margem média
- Alerta automático de estoque baixo (≤ 2 unidades)
- Tabela de todas as vendas do dia com horário, sabor, tipo, pagamento, total e lucro

### Vender
- Seleção de sabor/tamanho com estoque disponível exibido
- Escolha entre Congelada (preço normal) ou Assada (+R$2)
- Formas de pagamento: Dinheiro, Pix, Cartão Débito, Cartão Crédito
- Resumo em tempo real com preço unitário, total e lucro estimado
- Bloqueio automático se estoque insuficiente

### Estoque
- Tabela com quantidade atual e barra visual de nível por item
- Status: Sem estoque / Estoque baixo / OK
- Registro de entrada de mercadoria com atualização automática

### Cardápio
- Cadastro e edição de sabores com custo, preço congelada, preço assada e margem %
- Exclusão de itens (remove também do estoque)

### Histórico
- Todas as movimentações (vendas e entradas) com timestamp completo
- Filtro por tipo: Todos / Vendas / Entradas
- Auditoria de funcionários

## Dados

Tudo persistido em `localStorage` nas chaves:
- `pz_cardapio` — itens do cardápio
- `pz_estoque` — quantidades em estoque por item
- `pz_hist` — histórico de movimentações

## Dados iniciais

| Sabor | Tamanho | Custo | Congelada | Assada |
|---|---|---|---|---|
| Calabresa | Média | R$10 | R$15 | R$17 |
| Mussarela | Média | R$10 | R$15 | R$17 |
| Frango c/ Catupiry | Média | R$12 | R$18 | R$20 |
| Calabresa | Grande | R$16 | R$24 | R$27 |
| Mussarela | Grande | R$16 | R$24 | R$27 |
