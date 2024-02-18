# Exercício 16

[*Ver Algoritmo*](Algoritmo16.md)

 *Na matriz M10x10 abaixo, quatro números ao longo de uma linha diagonal
foram marcadas em negrito. O produto desses números é 1788696.*

$$\[
\begin{bmatrix}
    08 & 02 & 22 & 97 & 38 & 15 & 00 & 40 & 00 & 75 \\
    49 & 49 & 99 & 40 & 17 & 81 & 18 & 57 & 60 & 87 \\
    81 & 49 & 31 & 73 & 55 & 79 & 14 & 29 & 93 & 71 \\
    52 & 70 & 95 & 23 & 04 & 60 & 11 & 42 & 69 & 24 \\
    22 & 31 & 16 & 71 & 51 & 67 & \mathbf{14} & 89 & 41 & 92 \\
    24 & 47 & 32 & 60 & 99 & 03 & 45 & \mathbf{78} & 44 & 75 \\
    32 & 98 & 81 & 28 & 64 & 23 & 67 & 10 & \mathbf{26] & 38 \\
    67 & 26 & 20 & 68 & 02 & 62 & 12 & 20 & 95 & \mathbf{63} \\
    24 & 55 & 58 & 05 & 66 & 73 & 99 & 26 & 97 & 17 \\
    21 & 36 & 23 & 09 & 75 & 00 & 76 & 44 & 20 & 45 \\
\end{bmatrix}
\]$$

*Faça um pseudocódigo que preencha uma matriz 10x10 de números inteiros e apresente o maior produto de quatro números consecutivos na horizontal, vertical e diagonal, bem como os números que formam o produto.*

**Entrada**

- 100 números inteiros.

**Saída**

- O maior produto de 4 números consecutivos em cada uma das direções.

**Restrições**

- nenhuma

**Exemplo**


| Entrada | Saída |
|-|-|
| 1, 2, 3, 4, 5, …, 96, 97, 98, 99,100| Matriz: <BR>1 2 3 4 5 6 7 8 9 10<BR>11 12 13 14 15 16 17 18 19 20<BR>21 22 23 24 25 26 27 28 29 30<BR>31 32 33 34 35 36 37 38 39 40<BR>41 42 43 44 45 46 47 48 49 50<BR>51 52 53 54 55 56 57 58 59 60<BR>61 62 63 64 65 66 67 68 69 70<BR>71 72 73 74 75 76 77 78 79 80<BR>81 82 83 84 85 86 87 88 89 90<BR>91 92 93 94 95 96 97 98 99 100<BR>Maior produto da horizontal se encontra na 10ª linha:<BR>94109400 = 97 * 98 * 99 * 100<BR>Maior produto da vertical está na 10ªcoluna:<BR>50400000 = 70 * 80 * 90 * 100<BR>Maior produto da diagonal está na 7ª diagonal no sentido principal: 46511400 = 67 * 78 * 89 * 100|