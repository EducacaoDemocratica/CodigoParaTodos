# Exercício 12

[*Ver Algoritmo*](Algoritmo12.md)

 *Faça um pseudocódigo que gere uma matriz Identidade I 2x2 a partir de uma matriz M2x2. A matriz identidade é o resultado da multiplicação de uma matriz por sua inversa.*

**Entrada**

- 4 números inteiros.

**Saída**

- A impressão de uma matriz identidade I2x2, caso a matriz M possua inversa.

**Restrições**

- a matriz só possuirá inversa se o seu determinante não for nulo.

**Exemplo**

**Entrada:**

8, 9, 8, 2

**Saída**

Matriz Original:
 
$$\[
\begin{bmatrix}
     8 & 9 \\
	8 & 2 \\
\end{bmatrix}
\]$$ 

Matriz Inversa:
 
$$\[
\begin{bmatrix}
     -0.04 & 0.16 \\
	 0.14 & -0.14 \\
\end{bmatrix}
\]$$ 

Matriz Identidade:
 
$$\[
\begin{bmatrix}
     1 & 0 \\
	 0 & 1 \\
\end{bmatrix}
\]$$ 

**Entrada:**

1, 2, 3, 6

**Saída**

Matriz Original:
 
$$\[
\begin{bmatrix}
     1 & 2 \\
	3 & 6 \\
\end{bmatrix}
\]$$ 

A matriz não possui inversa.