# Exercício 28

[*Ver Algoritmo*](Algoritmo28.md)


 *Faça um pseudocódigo que apresente as n raízes (X<sub>n</sub>) do seguinte sistema
particular de n equações com n incógnitas:*

$$\
\begin{cases}
    a_{11}X_1 + a_{12}X_2 + a_{13}X_3 + \ldots + a_{1n}X_n = b_1 \\
     ( \dots ) + a_{22}X_2 + a_{23}X_3 + \ldots + a_{2n}X_n = b_2 \\
    ( \dots )+( \dots )+( \dots )+( \dots )+( \dots ) = ( \dots )\\    
    ( \dots )+( \dots )+( \dots ) +( \dots )+ a_{nn}X_n = b_n \\
\end{cases}
\$$

Onde:
- [b1, b2, b3, ... bn] é o vetor dos termos independentes;
-[a1n, a2n, a3n, ... ain] é a matriz triangular superior (valores da diagonal principal e acima dela) de coeficientes, com n variando de 1 até o número de equações desejadas;
- [X1, X2, X3, ... Xn] são as variáveis do sistema.

$$\
\begin{cases}
    -4x_1 + 3x_2 + 0x_3 - 4x_3 = -16 \\
    2x_2 - 1x_3 -2x_4 = 8 \\
     x_3 + x_4 = -7 \\
     3x_4 = 12 \\
\end{cases}
\$$

*Sendo fornecido na entrada o número n de equações (3 <= n <= 10), a matriz
inteira triangular A dos coeficientes e o vetor real B dos termos independentes,
apresente as n raízes do sistema.
Caso seja necessário, pesquise sobre escalonamento de sistemas lineares.*

**Entrada**

- O número n de raízes (a dimensão da matriz), a matriz triangular superior A e o
vetor B dos termos independentes.

**Saída**

- As n raízes do sistema (o vetor X).

**Restrições**

- n deve ser maior/igual a 3 e menor/igual a 10.

| Entrada | Saída |
|-|-|
|n: 4<BR><BRA: -4, 3, 0, -4<BR>2, -1, -2<BR>1, 1<BR>3<BR><BR>B: -16, 8, -7, 12|RAÍZES DO SISTEMA:<BR>X1: 1.875<BR>X2: 2.5<BR>X3: -11<BR>X4: 4|
|n: 6<BR>A: 2, -4, -4, 4, -4, 0<BR>3, 4, 5,<BR>1, -2<BR>-1, -4, 2, 3<BR>4, -3, -1<BR>1, -3<BR>-4<BR>B: 5, 5, -4, 1, 1, 3|RAÍZES DO SISTEMA:<BR>X1: 6<BR>X2: -0.625<BR>X3: 2.75<BR>X4: -0.875<BR>X5: -1.25<BR>X6: -0.75|
|n: 11|Erro: insira um valor de 3 a 10.|