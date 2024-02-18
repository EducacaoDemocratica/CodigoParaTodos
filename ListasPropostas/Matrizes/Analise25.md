# Exercício 25

[*Ver Algoritmo*](Algoritmo25.md)

 *Faça um pseudocódigo que permita jogar o jogo da velha contra o
computador. Aprimore as jogadas do computador, considerando as
possibilidades de jogo do oponente, deixando-as estratégicas e inteligentes. Por
exemplo, se o oponente tiver 2 símbolos em condições de fechar uma linha, o
computador pode fazer sua jogada naquela posição e interromper a chance de
vitória.*


**Entrada**

- O símbolo do jogador (“X” ou “O”) e suas jogadas.

**Saída**

- O vencedor do jogo, se houver.

**Restrições**

- o jogo não deve ultrapassar 9 rodadas.
- o jogador só pode utilizar o símbolo que escolheu.
- a cada jogada a matriz do jogo deve ser impressa.

**Exemplo**
<sub>Nota: as jogadas do computador não são lidas. Elas fazem parte da entrada somente para entender o
que se pede.

| Entrada | Saída |
|-|-|
|jog “O”<BR>comp: “X”<BR>//1ª jogada<BR>jog: 2, 2<BR>//2ª jogada//<BR>comp: 1, 3<BR>//3ª jogada<BR>jog: 1, 1<BR>//4ª jogada<BR>comp: 3, 3<BR>//5ª jogada<BR>jog: 2, 1O<BR>//6ª jogada//<BR>comp: 2, 3|//após 1ª rodada<BR>#	#	#<BR>#	 O	 #<BR> #	#	#<BR>//após 2ª rodada<BR># # X<BR># O #<BR># # #<BR>//após 3ª rodada<BR>O	#	X<BR>#	O	#<BR>#	#	#<BR>//após 4ª rodada<BR>O		#	X<BR>#	O	#<BR>#	#	X<BR>//após 5ª rodada<BR>O	#	X<BR>O	O	#<BR>#	#	X<BR>//após 6ª rodada<BR>O	#	X<BR>O	O	X<BR>#	#	X<BR>O computador (X) venceu!|