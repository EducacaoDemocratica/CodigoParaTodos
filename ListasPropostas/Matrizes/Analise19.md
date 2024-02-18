# Exercício 19

[*Ver Algoritmo*](Algoritmo19.md)

 *O jogo da Mega Sena é uma loteria onde o jogador marca no mínimo 6
números entre 1 e 60, sem repetição, em um cartão. A agência promotora do
jogo realiza um sorteio onde são escolhidos aleatoriamente 6 números, também
entre 1 e 60 e sem repetição. Se algum cartão de algum jogador contiver os
mesmos 6 números sorteados, ele leva o prêmio anunciado. Ganham premiação
também quem faz 5 ou 4 acertos.
Faça um pseudocódigo que receba 5 apostas de 6 números entre 1 e 60 sem
repetição. Apresente os números apostados em ordem crescente.*


**Entrada**

- Cinco apostas de 6 números inteiros.

**Saída**

- As cinco apostas impressas em ordem crescente.

**Restrições**

- os números devem pertencer ao intervalo [1, 60].
- uma aposta não deve conter dois números repetidos.

**Exemplo**


| Entrada | Saída |
|-|-|
|1ª aposta: 24, 14, 46, 12, 8, 10<BR>2ª aposta: 22, 28, 48, 37, 21,27<BR>3ª aposta: 30, 48, 45, 42, 55,19<BR>4ª aposta: 52, 44, 30, 46, 49,43<BR>5ª aposta: 36, 34, 45, 17, 26,35|Números da 1ª aposta: 8, 10, 12, 14,24,26<BR>Números da 2ª aposta: 21, 22, 27, 28,37,48<br>Números da 3ª aposta: 19, 30, 42, 45,48,45<BR>Números da 4ª aposta: 30, 43, 44, 46,49,52<BR>Números da 5ª aposta: 17, 26, 34, 35,36,45|
|1ª aposta: 36, 37, 42, 56, 41,25<BR>2ª aposta: 56, 31, 4, 54, 45, 61| Erro: Insira valorse entre 1 e 60|
|1ª aposta: 23, 34, 4, 10, 48, 9<BR>2ª aposta: 47, 2, 60, 41, 8,15<BR>3ª aposta: 55, 1, 12, 30, 9, 28<BR>4ª aposta: 43, 23, 27,49, 59,23|Erro: Essa aposta contém números repetidos. Insira outro número|