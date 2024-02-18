# Exercício 14

[*Ver Algoritmo*](Algoritmo14.md)

 *Quadrados Mágicos consistem em uma matriz quadrada em que as somas das linhas, das colunas e das diagonais principal e secundária são as mesmas.*

$$\[
\begin{bmatrix}
     6 & 1 & 9 \\
     7 & 5 & 3 \\
     2 & 9 & 4 \\
\end{bmatrix}
\]$$ 

*Note que a soma das linhas, colunas e diagonais dessa matriz é 15.*
*Faça um pseudocódigo que preencha uma matriz M 3x3 de números inteiros, seguramente sem repetições entre eles, e imprima se a matriz é um quadrado mágico ou não.*

**Entrada**

- 9 números inteiros.

**Saída**

- Se a matriz é um quadrado mágico ou não.

**Restrições**

- A matriz não deve conter elementos repetidos.

**Exemplo**


| Entrada | Saída |
|-|-|
| 8, 3, 4, 1, 5, 9, 6, 7, 2 |Matriz:<BR>8	3	4<BR>1	5	9<BR>6	7	2<BR>A matriz é um quadrado mágico e a soma das linhas, colunas e diagonais é 15.|
|1, 4, 9, 7, 6, 3, 2, 8, 5|Matriz:<BR>1	4	9<BR>7	6	3<BR>2	8	5<BR>A matriz não é um quadrado mágico.|