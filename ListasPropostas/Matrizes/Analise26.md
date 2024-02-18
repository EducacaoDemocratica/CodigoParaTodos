# Exercício 26

[*Ver Algoritmo*](Algoritmo26.md)

 *O campo minado é um jogo onde o participante deve evitar tocar em uma
posição do terreno que tem uma bomba. O terreno (uma matriz) é dividido em
células e suas bombas são distribuídas no terreno de forma aleatória. Quando o
jogador faz um movimento e aciona uma bomba, o jogador perde. Mas se não
acionar uma bomba, o jogo apresenta a quantidade de bombas existentes
diretamente na vizinhança horizontal, vertical ou diagonal do jogador. O jogo
encerra quando o jogador aciona uma bomba ou quando só restam bombas no
terreno, tendo o jogador encontrado todos os caminhos seguros possíveis.
Faça um pseudocódigo que distribua 7 bombas de forma aleatória em uma
matriz 5x5 e permita você jogar campo minado.*


**Entrada**

- O movimento do jogador (a coordenada, linha e coluna, para onde o jogador
deseja ir).

**Saída**

- A impressão da matriz a cada movimento até o jogador encontrar todos os
caminhos seguros ou até acionar uma bomba.

**Restrições**

- o jogador pode acessar apenas as linhas e colunas 1 até 5.
- o sistema deve mostrar apenas a quantidade de bombas na vizinhança do
jogador.

**Exemplo**
<sub>Nota: simulando o console do Visualg.

```
Início da execução<BR>
	
$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & * & * & *\\
    5 & * & J & * & * & *\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 5

Insira uma coluna: 1

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & * & * & *\\
    5 & J & X & * & * & *\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 5

Insira uma coluna: 2

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & * & * & *\\
    5 & X & J & * & * & *\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 5

Insira uma coluna: 3

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & * & * & *\\
    5 & X & X & J & * & *\\
\end{bmatrix}
\]$$

Existem 0 bombas ao seu redor.

Insira uma linha: 4

Insira uma coluna: 3

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & J & * & *\\
    5 & X & X & X & * & *\\
\end{bmatrix}
\]$$


Existem 1 bombas ao seu redor.

Insira uma linha: 4

Insira uma coluna: 4

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & X & J & *\\
    5 & X & X & X & * & *\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 5

Insira uma coluna: 4

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & X & X & *\\
    5 & X & X & X & J & *\\
\end{bmatrix}
\]$$

Existem 0 bombas ao seu redor.

Insira uma linha: 5

Insira uma coluna: 5

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & X & X & *\\
    5 & X & X & X & X & J\\
\end{bmatrix}
\]$$

Existem 0 bombas ao seu redor.

Insira uma linha: 4

Insira uma coluna: 5

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & X & X & J\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 4

Insira uma coluna: 4

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & X & J & X\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 4

Insira uma coluna: 3

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & * & *& * \\
    4 & * & * & J & X & X\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

Existem 1 bombas ao seu redor.

Insira uma linha: 3

Insira uma coluna: 3

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & J & *& * \\
    4 & * & * & X & X & X\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

Existem 2 bombas ao seu redor.

Insira uma linha: 4

Insira uma coluna: 2

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & X & *& * \\
    4 & * & J & X & X & X\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

Existem 2 bombas ao seu redor.

Insira uma linha: 3

Insira uma coluna: 3

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & * & *& * \\
    3 & * & * & J & *& * \\
    4 & * & X & X & X & X\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

Existem 2 bombas ao seu redor.

Insira uma linha: 2

Insira uma coluna: 3

$$\[
\begin{bmatrix}
   [ ] & 1 & 2 & 3 & 4 & 5 \\
    1 & * & * & * & *& * \\
    2 & * & * & B & *& * \\
    3 & * & * & J & *& * \\
    4 & * & X & X & X & X\\
    5 & X & X & X & X & X\\
\end{bmatrix}
\]$$

O JOGADOR PERDEU!

Fim da execução.