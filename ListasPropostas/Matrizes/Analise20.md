# Exercício 20

[*Ver Algoritmo*](Algoritmo20.md)

 *Faça um pseudocódigo que receba 10 apostas de 6 a 10 números entre 1 e
60, sem repetição, e que gere os 6 números sorteados, também entre 1 e 60 e
sem repetição. Apresente a quantidade de acertos que cada aposta teve em
relação aos números sorteados.*


**Entrada**

- Dez apostas de n números inteiros.

**Saída**

- A impressão dos 6 números sorteados e junto de cada aposta e da sua
porcentagem de acertos.

**Restrições**

- n deve ser maior ou igual a 6 e menor ou igual a 10
- os números devem pertencer ao intervalo [1, 60].
- uma aposta e o resultado de um sorteio não deve conter dois números repetidos.

**Exemplo**
<sub>Nota: utilizando 5 apostas na entrada, ambas com 6 números apostados.


| Entrada | Saída |
|-|-|
|1ª aposta:37, 57, 54, 19, 6,25<br>2ª aposta:41, 21, 34, 22, 4,12<br>3ª aposta:16,40,34,3,51,48<br>4ª aposta:49,30,20,41,18,40<BR>5ª aposta:36, 28, 31, 20, 10,51|Números da 1ª aposta: 6, 19, 25, 37,54, 57.<BR>Números da 2ª aposta: 4, 12, 21, 22,34, 41.<BR>Números da 3ª aposta: 3, 16, 34, 40,48, 51.<BR>Números da 4ª aposta: 18, 20, 30, 40,41, 49.<BR>Números da 5ª aposta: 10, 20, 28, 31,36, 57.<BR>Números sorteados: 6, 13, 22, 30, 32,35.<BR>A 1ª aposta acertou 1 dos 6 números sorteados.<BR>A 2ª aposta acertou 1 dos 6 números sorteados.<BR>A 3ª aposta acertou 0 dos 6 números sorteados.<BR>A 4ª aposta acertou 1 dos 6 números sorteados.<BR>A 5ª aposta acertou 0 dos 6 números sorteados.|1ª aposta: 45, 10, 9, 35, 6, 27<BR>2ª aposta: 49, 39, 7, 45, 43,37<BR>3ª aposta: 5, 43, 21, 25, 47,35,<BR>4ª aposta: 28, 48, 30, 56, 11,60,<br>5ª aposta: 48, 25, 2, 26, 54,68|Erro: insira valores entre 1 e 60:|Erro: insira valores entre 1 e 60:|
|1ª aposta:49, 54, 13, 38, 9,37<BR>2ª aposta:20, 56, 3, 54, 35,55<BR>3ª aposta:49, 5, 16, 14, 48,55<BR>4ª aposta:9, 35, 56, 46, 14,13<BR>5ª aposta:21, 51, 24, 9, 12,21| Erro: essa aposta contém números repetidos. Insira um outro número|



