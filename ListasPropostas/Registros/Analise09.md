# Exercício 09

[*Ver Algoritmo*](Algoritmo09.md)

 *Faça um pseudocódigo que armazene em um registro o código, nome (de até 15 caracteres), preço e a quantidade em estoque de 5 produtos. Realize 3 pedidos, compostos por um código de produto, a quantidade desejada. Localize o código e, se houver quantidade suficiente para atender ao pedido integralmente, atualize o estoque e informe o usuário. Se não for possível atender ao pedido, exiba uma mensagem informando qual erro ocorreu.*

**Entrada**

- O código, nome, preço e quantidade de cada um dos 5 produtos e o código do produto e a quantidade desejada de um pedido.

**Saída**

- A impressão dos dados do pedido e dos produtos após a atualização do estoque.

**Restrições**

- não devem ser aceitos nomes e códigos repetidos.
- não deve ser aceito nenhum valor negativo ou nulo.
- um pedido só é realizado se o código for de algum produto existente e se houver
- a quantidade em estoque o suficiente para atender a quantia desejada

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|//código, nome, preço, estoque<br>produto 1: 001, “Caneta azul”, 2.50,20<br>produto 2: 002, “Caderno de 10 matérias”, 19.99, 50<br>produto 3: 003, “Máscara capilar”,23.90, 14<br>produto 4: 004, “Ativador de cachos”, 15.90, 8<br>produto 5: 005, “Mochila escolar”,60.00, 10<br>//código do produto, quantidade<br>pedido 1: 008, 10<br>pedido 2: 003, 15<br>pedido 3: 004, 1|PEDIDO 1<br>Produto: DESCONHECIDO. (CÓD 8).<br>Quantidade: 0.<br>Status:<br>ERRO: PRODUTO NÃO ENCONTRADO!<br>Valor: R$ 0.|
|produto 1: 004, “Lápis de cor”, 7.50, 10<br>produto 2: 004|Erro: código inválido. Preencha esse campo corretamente:|
|produto 1: 002, “Mousepad”, 39.90, 10<br>produto 2: 008,“Mousepad”|Erro: nome inválido. Preencha esse campo corretamente:|
|produto 1: 007, “Tesoura”, 5.50, -1|Erro: estoque inválido. Preencha esse campo corretamente:|