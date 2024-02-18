# Exercício 29

[*Ver Algoritmo*](Algoritmo29.md)

*O dono do quiosque tem uma tabela onde armazena o preço de cada um dos 9 produtos. Faça um pseudocódigo que armazene os preços e as vendas diárias de cada produto e informe::*

*a. O total vendido no dia.*<br>

*b. O produto que deu maior retorno financeiro.*<br>

*c. A diferença no valor arrecadado entre o produto que deu maior retorno e o produto mais vendido.*<br>

**Entrada**

- O preço e a quantidade vendida de cada um dos produtos.

**Saída**

- O total vendido no dia, o produto que deu maior retorno, a diferença na arrecadação do produto mais vendido e do produto que deu maior retorno financeiro.

**Restrições**

- A quantidade vendida não pode ser negativa.
- o valor de um produto deve ser maior que 0.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|preços: 37.98, 65.58, 17.58,<br>54.49, 27.02, 87.28, 35.02,93.38,
16.98..<br>vendas: 88, 7, 72, 20, 13, 69, 33,3, 49.|Total vendido: R$ 14798.26<br>O produto que deu maior retorno foi o 6º com R$ 6022.32<br>O produto mais vendido arrecadou: R$3342.24<br>A diferença na arrecadação entre o produto de retorno e o mais vendido é R$2680.08.|
|preços: 15.67, 58.94, 9.08, 78.87,89.41, 19.12, 44.66, 50.68, 13.09.<br>vendas: 32, 57, 97, 99, 3, 70, 12,67, 51.|Total vendido: R$ 18755.61<br>O produto que deu maior retorno foi o 4º com R$ 7808.13<br>O produto mais vendido é o mesmo de maior retorno
financeiro.|
|preços: 54.55, 18.96, 63.24, 72.65, E26.53, 81.48, 54.99, 70.6, 0.|Erro: o preço deve ser maior que 0. Insira outro:|
|preços: 65.27, 80.2, 78.3, 98.79,53.91, 67.39, 16.45, 16.85, 3.33.<br>vendas: -1, 68, 82, 90, 38, 84, 60,26, 24.|Erro: a quantidade vendida não pode ser negativa. Insira outro valor:|

