# Exercício 09

[*Ver Algoritmo*](Algoritmo09.md)

 *Faça um pseudocódigo que receba duas matrizes A CxD e BFXG sendo que os valores C, D, E e F são informados pelo usuário e vão de 1 até 6Verifique se o produto matricial de A por B é possível e, caso seja possível, calcule o tal produto, imprimindo a matriz HCxG resultado.*

**Entrada**

- Os números inteiros C, D, F e G, os CxD valores da matriz A e os FxG valores da
matriz B.

**Saída**

- A impressão do produto matricial, se ele existir.

**Restrições**

- C, D, F e G vão de 1 até 6.
- o produto matricial só existe se D for igual a F.

**Exemplo**


| Entrada | Saída |
|-|-|
|C: 5<BR>D: 6<BR>F: 4<BR>G: 2<BR>matriz A:<BR>9, 6, 8, 9, 9, 2,<BR>8, 2, 9, 6, 7, 6,<BR>3, 1, 2, 9, 3, 5,<BR>4, 1, 4, 5, 3, 1,<BR>8, 2, 4, 5, 8, 7<BR>matriz B:<BR>1, 8,<BR>3, 7,<BR>6, 0,<BR>9, 3|Não é possível realizar o produto matricial entre A e B.|
|C: 1<BR>D: 6<BR>F: 6<BR>G: 6<BR>matriz A:<BR>1, 3, 9, 2, 8, 5<BR>matriz B:<BR>6, 1, 4, 2, 8, 4,<BR>5, 8, 7, 8, 0, 5,<BR>0, 6, 9, 3, 4, 2,<BR>1, 7, 7, 7, 1, 8,<BR>5, 7, 3, 8, 5, 6,<BR>8, 3, 3, 8, 3, 3|Matriz H/produto: 6	1	4	2	8	4|
|C: 1<BR>D: 3<BR>F: 4<BR>G: 0|Erro: insira valores entre 1 e 6:|
|C: 5<BR>D: 3<BR>F: 5<BR>G: 7|Erro: insira valores entre 1 e 6:|


