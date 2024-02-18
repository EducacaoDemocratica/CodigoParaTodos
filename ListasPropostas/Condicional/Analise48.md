# Exercício 48

[**Ver Algoritmo**](Algoritmo48.md)

*No jogo de par ou ímpar, 2 jogadores colocam valores aleatórios entre 0 e 5 e ganha quem descobrir se a soma dos valores será um número par ou ímpar. Faça um pseudocódigo que permita um usuário jogar par ou ímpar com o computador. Para evitar que um saiba a resposta do outro, o computador irá sortear o valor que colocará antes do jogador colocar seu valor. Ganha quem conseguir mais vitórias em uma rodada de 5 jogadas.Pesquise sobre a função randi() do Visualg.*

**Entrada:**
- Os números escolhidos pelo usuário e as apostas (ímpar ou par)..

**Saída:**
- O vencedor das cinco rodadas se houver.

**Restrições:**
- os números devem ser somente de 0 a 5, as apostas só devem assumir “ímpar” ou “par”.

*Nota: os dados do computador não são lidos, eles estão na entrada abaixo somente para facilitar a compreensão do que se pede*
**Exemplo:**
| Entrada | Saída |
| ------- | ----- |
| Computador: 5, “Ímpar”<br>Jogador: 3, “Par”;<br><br>Computador: 4, “Ímpar”<br>Jogador: 1, “Ímpar””;<br><br>Computador: 5, “Ímpar”<br>Jogador: 3, “par”;<br><br>Computador: 5, “par”<br>Jogador: 3, “par”;<br><br>Computador: 0, “Ímpar”<br>Jogador: 0, “Ímpar”; |O jogador venceu. |
| Computador: 3, “par”<br>Jogador: 5, “Par”;<br><br>Computador: 1, “Ímpar”<br>Jogador: 1, “par””;<br><br>Computador: 2, “par”<br>Jogador: 0, “Ímpar”;<br><br>Computador: 5, “par”<br>Jogador: 4, “par”;<br><br>Computador: 0, “Ímpar”<br>Jogador: 0, “Ímpar”; | Empate|
| Computador:3, “Par”<br>Jogador:6,"A" | Erro: coloque valores de 0 a 5 no número escolhido.<br>Erro: valor inválido para aposta. |
