# Exercício 43

[*Ver Algoritmo*](Algoritmo43.md)

*O jogo da Mega Sena é uma loteria onde o jogador marca no mínimo 6 números entre 1 e 60, sem repetição, em um cartão. A agência promotora do jogo realiza um sorteio onde são escolhidos aleatoriamente 6 números, também entre 1 e 60 e sem repetição. Se algum cartão de algum jogador contiver os mesmos 6 números sorteados, ele leva o prêmio anunciado. Ganham premiação também quem faz 5 ou 4 acertos.Faça um pseudocódigo que receba 1 aposta de 6 números entre 1 e 60 sem repetição. Apresente os números apostados em ordem crescente.*



**Entrada**

- A aposta de 6 números inteiros.

**Saída**

- A aposta impressa em ordem crescente.

**Restrições**

- os números devem pertencer ao intervalo [1, 60].
- uma aposta não deve conter dois números repetidos.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|27, 36, 49, 37, 16, 2.|Números da aposta: 2, 16, 27, 36, 37, 49.|
|8, 3, 7, 3, 28, 3.|Erro: esse valor já está na aposta. Insira outro:|
|40, 68, 5, 26, 27, 18.|Erro. Insira valores de 1 a 60:|
|0, 22, 27, 37, 18, 32|.Erro. Insira valores de 1 a 60:|