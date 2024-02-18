# Exercício 32

[*Ver Algoritmo*](Algoritmo32.md)

*Um armazém trabalha com 100 mercadorias diferentes identificadas pelos números inteiros de 1 a 100. O dono do armazém anota a quantidade de cada mercadoria vendida durante o mês. Ele tem uma tabela que indica para cada mercadoria o preço de venda. Faça um pseudocódigo que receba o identificador,o preço e a quantidade vendida de cada mercadoria e imprima as 10 mercadorias mais vendidas, as 10 mercadorias de maior valor e o faturamento mensal do armazém.*

**Entrada**

- O identificador, o preço e a quantidade vendida de cada mercadoria.

**Saída**

- O faturamento mensal do armazém e os 10 produtos mais vendidos e os 10 menos vendidos

**Restrições**

- os identificadores dos produtos vão de 1 a 100 e não devem se repetir.
- a quantidade vendida não deve ser negativa.
- o preço de um produto deve ser maior que zero.


**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|identificadores: 75, 30, 10, 54, 47,27, 4, 2, 65, 52.<br>quantidades: 93, 100, 49, 62, 95,37, 68, 15, 67, 34.<br>preços: 86.93, 44.07, 71.15, 50.55, 100.76, 65.61, 73.34, 11.73, 56.35,30.77.|Faturamento mensal: R$41096.41.<br>Os 10 produtos mais vendidos:<br>Produto 2 com 15 unidades.<br>Produto 52 com 34 unidades.<br>Produto 27 com 37 unidades.<br>Produto 10 com 49 unidades.<br>Produto 54 com 62 unidades.<br>Produto 65 com 67 unidades.<br>Produto 4 com 68 unidades.<br>Produto 75 com 93 unidades.<br>Produto 47 com 95 unidades.<br>Produto 30 com 100 unidades.<br>Os 10 produtos de maior valor:<br>Produto 2 de preço R$ 11.73.<br>Produto 52 de preço R$ 30.77.<br>Produto 30 de preço R$ 44.07.<br>Produto 54 de preço R$ 50.55.<br>Produto 65 de preço R$ 56.35.<br>Produto 27 de preço R$ 65.61.<br>Produto 10 de preço R$ 71.15.<br>Produto 4 de preço R$ 73.34.<br>Produto 75 de preço R$ 86.93<br>Produto 47 de preço R$100.76|
|identificadores: 49, 41, 98, 42, 13,33, 86, 67, 25, 102.|Erro: os identificadores vão de 0 a 100. Insira outro:|
|identificadores: 84, 86, 47, 19, 48,16,66,97,39,86<br>|Erro: esse identificador já foi usado.Insira outro:|
|identificadores: 58, 69, 47, 73, 25, 54, 24, 19, 88, 8.<br>quantidades: 0, 54, 77, 63, 22, 99, 56, 73, 79, -5.|Erro: a quantidade vendida não deve ser negativa. Insira outra:|
|identificadores: 55, 63, 43, 54, 64, 5, 93, 13, 9, 10.<br>quantidades: 85, 78, 6, 88, 84, 51,47, 3, 59, 85.<br>preços: 20.78, 0, 71.41, 43.89,21.77, 75.2, 86.05, 43.83, 78.12,64.16|Erro: o preço deve ser maior que 0. Insira outro:|