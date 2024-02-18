# Exercício 54

[*Ver Algoritmo*](Algoritmo54.md)

*O jogo de cartas 21 é um clássico com várias versões. Em uma das versões utiliza-se cartas entre 2 e 10 de 4 naipes, ou seja, para cada número existem 4 cartas. Cada jogador recebe 3 cartas de forma aleatória, das quais ele pode trocar no máximo 2. Ganha quem chegar mais próximo da soma de 21 com as cartas que tem na mão. Faça um pseudocódigo que permita ao usuário jogar o 21 com o computador.*

**Entrada**

- A quantidade q de cartas que o jogador deseja trocar e a(s) carta(s) que deseja trocar.

**Saída**

- O vencedor da disputa.

**Restrições**

- q não deve ser negativo nem maior que 2.
- o jogador só pode trocar o número de cartas que ele escolheu.
- o jogador só pode trocar as cartas que ele tem em mãos.

**Exemplo**
*Nota: as cartas do jogador e do computador não são lidas, elas estão na entrada abaixo somente para facilitar a compreensão do que se pede.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|computador: 2, 7, 3.<br>jogador: 6, 3, 4.<br>q: 0.|O jogador venceu!|
|computador: 9, 8, 6.<br>jogador: 5, 5, 3.<br>q: 0.|O computador venceu!|
|computador: 2, 8, 6.<br>jogador: 3, 9, 4.<br>q: 0.|Empate!|
|//1ª interação com o console<br>computador: 4, 3, 7.<br>jogador: 7, 6, 4.<br>q: 1.<br>//2ª interação com o console<br>c1: 4.|//1ª interação com o console<br>Escolha a carta que deseja trocar:<br>//2ª interação com o console<br>Carta trocada: 4 -> 7.<br>O jogador venceu!|//1ª interação com o console<br>computador: 6, 5, 7.<br>jogador: 3, 2, 8.<br>q: 3.<br>//2ª interação com o console<br>q: 2<br>//3ª interação com o console<br>c1: 4.<br>//4ª interação com o console<br>c1: 2.<br>//5ª interação com o console<br>c2: 2.<br>//6ª interação com o console<br>c2: 3.|//1ª interação com o console<br>Selecione 0, 1 ou 2:<br>//2ª interação com o console<br>Escolha a carta que deseja trocar:<br>//3ª interação com o console<br>Você não possui essa carta, insira outra.<br>//4ª interação com o console<br>2 -> 5.<br>//5ª interação com o console<br>Você não possui essa carta, insira outra.<br>//6ª interação com o console<br>3 -> 1.<br>O computador venceu!<br>|