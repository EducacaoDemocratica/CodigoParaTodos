# Exercício 30

[*Ver Algoritmo*](Algoritmo30.md)

*Ainda no quiosque, o dono fez uma nova tabela com o nome do produto,além da tabela com os preços. Faça um pseudocódigo que armazene os nomes,os preços e as vendas diárias de cada produto e informe::*

*a.O nome do produto com menor quantidade de vendas. Se tiver mais de 1, apresente os nomes de todos.*<br>

*b. Os nomes dos produtos e os preços de venda, em ordem alfabética.*<br>

*c. As quantidades de vendas e os nomes dos produtos, em ordem crescente de quantidade vendida.*<br>

**Entrada**

- O nome, preço e a quantidade vendida de cada um dos produtos.

**Saída**

- Os nomes dos produtos que menos venderam, os preços e os nomes de cada produto ordenados por ordem alfabética, a quantidade vendida e os nomes de cada produtos ordenados por ordem crescente de venda.

**Restrições**

- A quantidade vendida não pode ser negativa.
- o valor de um produto deve ser maior que 0.
- o nome não pode ser repetido ou vazio.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|nomes: batata frita, camarão, peixe , açaí, sorvete, sapatos, placas decoradas, brinquedos,pulseiras.<br>preços: 17.57, 4.61, 64.59, 30.83,97.57, 42.78, 20.27, 39.86, 45.81.<br>vendas: 18, 23, 66, 32, 39, 90, 9,16, 70.|Produto(s) mais vendido(s): sapatos.<br>Produtos e preços em ordem alfabética:
açaí- R$ 30.83.<br>batata frita - R$ 17.57.<br>brinquedos - R$ 39.86.<br>camarão - R$ 4.61.<br>peixe - R$ 64.59.<br>placas decoradas - R$ 20.27.<br>pulseiras - R$ 45.81.<br>sapatos - R$ 42.78.<br>sorvete - R$ 97.57.<br><br>Produtos e vendas em ordem
crescente de venda:<br>placas decoradas - 9 vendas.<br>brinquedos - 16 vendas.<br>batata frita - 18 vendas.<br>camarão - 23 vendas.<br>açaí - 32 vendas.<br>sorvete - 39 vendas.<br>peixe - 66 vendas.<br>pulseiras - 70 vendas.<br>sapatos - 90 vendas.|
|nomes: café, coca-cola, bombom, chinelo, quadro, camiseta, caderno, cordão, café.|Erro: esse produto já está cadastrado. Insira outro:|
|nomes: “”, camarão, peixe , açaí,sorvete, sapatos, placas decoradas,brinquedos, pulseiras|Erro: preencha esse campo:|
