# Exercício 53

[*Ver Algoritmo*](Algoritmo53.md)

*Seja P:*

*Faça um pseudocódigo que leia o valor de n, sendo n ≤ 21, e gere n coeficientes a. Calcule o valor de P para 10 valores de x e apresente o valor de P para cada x
correspondente.*

$$\[ P = a_n \cdot x^n + a_{n-1} \cdot x^{n-1} + a_{n-2} \cdot x^{n-2} + \ldots + a_1 \cdot x + a_0 \]$

**Entrada**

- Um número inteiro n e 10 números inteiros para x.

**Saída**

- O valor de P para cada x.

**Restrições**

- n deve ser maior que zero e menor/igual a 21.

**Exemplo**
*Nota: os valores de a não são lidos, eles estão na entrada abaixo somente para facilitar a compreensão do que se pede.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|n: 10<br>a: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.<br>x: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10|Para x = 1, P = 55.<br>Para x = 2, P = 18434.<br>Para x = 3, P = 841449.<br>Para x = 4, P = 13514980.<br>Para x = 5, P = 119018555.<br>Para x = 6, P = 711082230.<br>Para x = 7, P = 3240618829.<br>Para x = 8, P = 12096030344.<br>Para x = 9, P = 38735995455.<br>Para x = 10, P = 109876543210|
|n: 0|Erro: o valor de n deve estar entre 1 e 21.|
|n: 22|Erro: o valor de n deve estar entre 1 e 21.|