# Exercício 44

[*Ver Algoritmo*](Algoritmo44.md)

*Faça um pseudocódigo que receba uma aposta de 6 a 10 números, entre 1 e 60, sem repetição. O usuário informará qual a quantidade números que deseja apostar.*

**Entrada**

- Um número inteiro n fornecido pelo usuário e uma aposta de n números inteiros.

**Saída**

- A aposta impressa em ordem crescente.

**Restrições**

- n deve ser maior ou igual a 6 e menor ou igual a 10.
- os números devem pertencer ao intervalo [1, 60].
- uma aposta não deve conter dois números repetidos.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|n: 9.<br>n-números: 15, 46, 56, 43, 21, 1, 11, 22, 31.|Números da aposta: 1, 11,15, 21, 22, 31, 43, 46, 56.|
|n: 5|Erro: insira de 6 a 10 números em sua aposta:|
|n: 11|Erro: insira de 6 a 10 números em sua aposta:|
|n: 6<br>n-números: 25, 52, 60, 60, 17, 3.|Erro: esse valor já está na aposta.Insira outro:|
|n: 7<br>n-números: 4, 30, 24, 53, 35, 27, 66.|Erro. Insira valores de 1 a 60:|