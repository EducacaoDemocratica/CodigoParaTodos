# Exercício 46

[*Ver Algoritmo*](Algoritmo46.md)

*Faça um pseudocódigo que receba uma aposta de 6 a 10 números entre 1 e 60, sem repetição, e que gere os 6 números sorteados, também entre 1 e 60 e sem repetição. Apresente a quantidade de acertos que a aposta teve em relação aos números sorteado*

**Entrada**

- Um número inteiro n fornecido pelo usuário e uma aposta de n números inteiros.

**Saída**

- A quantidade de acertos da aposta em relação ao resultado sorteado.

**Restrições**

- n deve ser maior ou igual a 6 e menor ou igual a 10.
- os números devem pertencer ao intervalo [1, 60].
- uma aposta e o resultado de um sorteio não deve conter dois números repetidos.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
| n: 6<br>n-números: 54, 10, 23, 31,37, 40.|Números sorteados: 23, 30, 43, 52, 53,55.<br>O jogador acertou 1 dos 6 números sorteados.|
| n: 10<br>n-números: 46, 3, 4, 34, 35, 37, 18, 50, 19, 26.|Números sorteados: 9, 16, 20, 23, 41,48.<br>O jogador acertou 0 dos 6 números sorteados.|
| n: 8<br>n-números: 2, 4, 53, 52, 67, 28, 27, 48.|Erro: insira de 6 a 10 números em sua aposta:|
| n: 7<br>n-números: 29, 60, 16, 5, 13, 53, 53.|Erro: esse valor já está na aposta. Insira outro:|