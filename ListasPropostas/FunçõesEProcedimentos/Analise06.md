# Exercício 06

[**Ver Algoritmo**](Algortimo06.md)

*Em um tabuleiro 8x8, uma peça tem sempre 8 possibilidades de movimento em
sua vizinhança. Faça um pseudocódigo usando módulos que posicione uma peça na
parte inferior no tabuleiro e permita chegar à extremidade superior distribuindo de 5
a ATÉ 20 bombas pelo tabuleiro de forma aleatória. Movimente a peça uma casa por
vez, sempre na sua vizinhança, indicando o número de bombas ao redor da peça. Se
na casa desejada houver uma bomba, a peça volta à primeira casa do tabuleiro, mas
a bomba fica desarmada. Informe a quantidade de movimentos feitos pelo jogador.*



**Entrada**

- A quantidade n de bombas a serem distribuídas e as coordenadas da casa (linha,
coluna).


**Saída**

- A quantidade de movimentos realizados pelo jogador.
  
**Restrições**

- n deve ser maior/igual a 5 e menor/igual a 20;
- faça as movimentações somente nas casas vizinhas;
- uma bomba desarmada não tem efeito.

**Exemplo**
<sub>Nota: simulando o console do visualg

Início da Execução<BR>
Insira a quantidade de bombas: 20<BR>


$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & * & * & * & * & * & * & * & * \\
3 & * & * & * & * & * & * & * & * \\
4 & * & * & * & * & * & * & * & * \\
5 & * & * & * & * & * & * & * & * \\
6 & * & * & * & * & * & * & * & * \\
7 & * & * & * & * & * & * & * & * \\
8 & * & J & * & * & * & * & * & * \\
\end{array}$$

Existem 2 bombas ao seu redor.<BR><BR>
Insira uma linha: 7<BR>
Insira uma coluna: 2<BR>

$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & * & * & * & * & * & * & * & * \\
3 & * & * & * & * & * & * & * & * \\
4 & * & * & * & * & * & * & * & * \\
5 & * & * & * & * & * & * & * & * \\
6 & * & * & * & * & * & * & * & * \\
7 & * & J & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$


Existem 3 bombas ao seu redor.<BR><BR>
Insira uma linha: 6<BR>
Insira uma coluna: 2<BR>


$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & * & * & * & * & * & * & * & * \\
3 & * & * & * & * & * & * & * & * \\
4 & * & * & * & * & * & * & * & * \\
5 & * & * & * & * & * & * & * & * \\
6 & * & J & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$

Existem 3 bombas ao seu redor.<BR><BR>
Insira uma linha: 5<BR>
Insira uma coluna: 2<BR>

$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & * & * & * & * & * & * & * & * \\
3 & * & * & * & * & * & * & * & * \\
4 & * & * & * & * & * & * & * & * \\
5 & * & J & * & * & * & * & * & * \\
6 & * & X & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$

Existem 3 bombas ao seu redor.<BR><BR>
Insira uma linha: 4<BR>
Insira uma coluna: 2<BR>

$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & * & * & * & * & * & * & * & * \\
3 & * & * & * & * & * & * & * & * \\
4 & * & J & * & * & * & * & * & * \\
5 & * & X & * & * & * & * & * & * \\
6 & * & X & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$

Existem 4 bombas ao seu redor.<BR><BR>
Insira uma linha: 3<BR>
Insira uma coluna: 2<BR>


$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & * & * & * & * & * & * & * & * \\
3 & * & J & * & * & * & * & * & * \\
4 & * & X & * & * & * & * & * & * \\
5 & * & X & * & * & * & * & * & * \\
6 & * & X & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$

Existem 5 bombas ao seu redor.<BR><BR>
Insira uma linha: 2<BR>
Insira uma coluna: 1<BR><BR>
BOMBA DESARMADA!<BR>

$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & B & * & * & * & * & * & * & * \\
3 & * & X & * & * & * & * & * & * \\
4 & * & X & * & * & * & * & * & * \\
5 & * & X & * & * & * & * & * & * \\
6 & * & X & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & J & * & * & * & * & * & * \\
\end{array}$$


Existem 2 bombas ao seu redor.<BR><BR>
...+ 6 movimentos...<BR>


$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & * & * & * & * & * & * & * & * \\
2 & J & * & * & * & * & * & * & * \\
3 & * & X & * & * & * & * & * & * \\
4 & * & X & * & * & * & * & * & * \\
5 & * & X & * & * & * & * & * & * \\
6 & * & X & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$

Existem 1 bombas ao seu redor.<BR><BR>
Insira uma linha: 1<BR>
Insira uma coluna: 1<BR>

$$\begin{array}
@ & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\
1 & J & * & * & * & * & * & * & * \\
2 & X & * & * & * & * & * & * & * \\
3 & * & X & * & * & * & * & * & * \\
4 & * & X & * & * & * & * & * & * \\
5 & * & X & * & * & * & * & * & * \\
6 & * & X & * & * & * & * & * & * \\
7 & * & X & * & * & * & * & * & * \\
8 & * & X & * & * & * & * & * & * \\
\end{array}$$

O jogador fez 13 movimentos.<BR>
Fim da execução.








