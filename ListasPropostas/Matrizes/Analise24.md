# Exercício 24

[*Ver Algoritmo*](Algoritmo24.md)

 *Jogo da velha é um jogo de estratégia em que é necessário colocar três
símbolos iguais em sequência em uma matriz 3x3 para ser declarado vencedor,
seja na linha, coluna ou diagonal. Faça um pseudocódigo que permita a 2
pessoas jogarem o jogo da velha. O código deve conferir a cada jogada se existe
um jogador vencedor*


**Entrada**

- O símbolo de cada jogador (“X” ou “O”) e as jogadas dos 2 players.

**Saída**

- O vencedor do jogo se houver.

**Restrições**

- o jogo não deve ultrapassar 9 rodadas;
- uma posição ocupada não pode ser selecionada novamente;
- os símbolos aceitos são somente “X” e “O”;
- a cada jogada a matriz do jogo deve ser impressa.

**Exemplo**


| Entrada | Saída |
|-|-|
|jog1: “X”<BR>jog2: “O”<BR>//1ª jogada<BR>jog1: 1, 1<BR>//2ª jogada<BR>jog2: 1, 2<BR>//3ª jogada<BR>jog1: 2, 2<BR>//4ª jogada<BR>jog2: 1, 3<BR>//5ª jogada<BR>jog1: 3, 3|//após 1ª rodada<BR>X # #<BR># # #<BR># # #<BR>//após 2ª rodada<BR>X O #<BR># # #<BR># # #<BR>//após 3ª rodada<BR>X O #<BR># X #<BR># # #<BR>//após 4ª rodada<BR>X O O<BR># X #<BR># # #<BR>//após 5ª rodada<BR>X O O<BR># X #<BR># # X<BR>O jogador 1 (X) venceu!|
|jog1: “O”<BR>jog2: “X”<BR>//1ª jogada<BR>jog1: 4, 1|Erro: essa posição não existe. Insira o valor da linha e da coluna de 1 até 3:|
|jog1: “X”<BR>jog2: “O”<BR>//1ª jogada<BR>jog1: 1, 1<BR>//2ª jogada<BR>jog2: 1, 1|Erro: essa posição já foi ocupada. Insira outra posição:|