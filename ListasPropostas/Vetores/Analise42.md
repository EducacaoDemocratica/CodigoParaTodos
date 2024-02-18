# Exercício 42

[*Ver Algoritmo*](Algoritmo42.md)

*Faça um pseudocódigo que armazene ATÉ 30 números inteiros, sem repetição, em um vetor A e ATÉ 20 números inteiros, sem repetição, em um vetor B. O usuário irá informar quantos números serão fornecidos.*
*Gere um vetor C que corresponde à união entre A e B (A U B). Imprima A, B e C em ordem crescente.*



**Entrada**

- Um número inteiro n fornecido pelo usuário, n-números inteiros, um inteiro m fornecido pelo usuário e m-números inteiros .

**Saída**

- A impressão dos vetores A, B e C em ordem crescente.

**Restrições**

- Nenhuma.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|n: 8<br>n-números: 19, 17, 14, 20, 12, 8,2, 4.<br>m: 3<br>m-números: 15, 18, 6.|A: 2, 4, 8, 14, 17, 19, 20, 21.<br>B: 6, 15, 18.<br>C: 2, 4, 6, 8, 14, 15, 17, 18, 19,20,21|
|n: 31.|Erro: Insira um número maior que 0 e menor/igual a 30:|
|n: 7.<br>n-números: 18, 9, 8, 21, 28, 13, 7.<br>m: 21|Erro: Insira um número maior que 0 e menor/igual a 20:|
|n: 9.<br>n-números: 9, 14, 3, 16, 13, 7, 29,20, 15.<br>m: 10.<br>
m-números: 4, 30, 21, 27, 23, 12,18, 14, 2, 2.|Erro: esse valor já está no vetor. Insira outro:|