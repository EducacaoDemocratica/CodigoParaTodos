# Exercício 15

[*Ver Algoritmo*](Algoritmo15.md)

 *O triângulo de Pascal é um triângulo aritmético infinito onde todo número
que faz parte do triângulo é um resultado da soma dos dois números que estão
na linha imediatamente acima dele. Começa com o número 1 e cada linha tem a
quantidade de números designados pela posição de sua linha, assim linha 1 tem
1 número, linha 2, 2 números e assim por diante.*

$$\[
\begin{array}{cccccccccc}
    &   &   &   & 1 &   &   &   &   &   \\
    &   &   & 1 &   & 1 &   &   &   &   \\
    &   & 1 &   & 2 &   & 1 &   &   &   \\
    & 1 &   & 3 &   & 3 &   & 1 &   &   \\
    1 &   & 4 &   & 6 &   & 4 &   & 1 &   \\
    & \vdots & & & & & & & \vdots & \\
\end{array}
\]$$

*Triângulo de pascal de 6 linhas.*
*Faça um pseudocódigo em Visualg que apresente um triângulo de Pascal de ATÉ 20 linhas. O valor deve ser informado pelo usuário.*

**Entrada**

- Um número inteiro n.

**Saída**

- Um triângulo de pascal de n linhas.

**Restrições**

- n deve ser maior que 0 e menor ou igual a 20.

**Exemplo**


| Entrada | Saída |
|-|-|
| 10 | 1<BR>1	1<BR>1	2	1<BR>1	3	3	1<BR>1	4	6	4	1<BR>1 5 10 10 5 1<BR>1 6 15 20 15 6 1<BR>1 7 21 35 35 21 7 1<BR>1 8 28 56 70 56 28 8 1<BR>1 9 36 84 126 126 84 36 9 1|
| 2|Triângulo de Pascal gerado:<BR>1<BR>1	1|
|0|Erro: insira valores de 1 até 20:|
|21|Erro: insira valores de 1 até 20:|