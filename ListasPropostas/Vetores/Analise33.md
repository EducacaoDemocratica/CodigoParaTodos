# Exercício 33

[*Ver Algoritmo*](Algoritmo33.md)

*Uma grande firma deseja saber quais os cinco empregados mais recentes. Faça um pseudocódigo que armazene o identificador único e o número de meses de trabalho de 6 a até 300 empregados e imprima os três mais recentes. Admita que não existem dois empregados admitidos no mesmo mês. O usuário irá informar quantos números serão fornecidos.*

**Entrada**

- Um número inteiro n fornecido pelo usuário e o identificador e a quantidade de meses trabalhados de cada um dos n empregados.

**Saída**

-  Os 5 empregados mais recentes.

**Restrições**

- n deve ser maior/igual a 6 e menor/igual a 300.
- os  identificadores e os números de meses não devem se repetir.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|n: 8 <br>identificadores: 55, 25, 53,87, 66, 15, 41, 16.<br>meses: 24, 19, 96, 74, 72, 60,89, 71.|Os 5 empregados mais recentes:<br>Identificador: 25 - Meses trabalhados 19.<br>Identificador: 55 - Meses trabalhados 24.<br>Identificador:15<br> - Meses trabalhados 60.<br>Identificador: 16 - Meses trabalhados 71.<br>Identificador: 66 - Meses trabalhados 72.|
|n: 5.|Erro: a quantia deve ser de 6 a 300.<br>Insira outra:|
|n: 301.|Erro: a quantia deve ser de 6 a 300.<br>Insira outra:|
|n: 12.<br>identificadores: 12, 93, 94,64, 33, 79, 89, 49, 23, 28, 38,0|.Erro: os identificadores devem ser maiores que 0. Insira outro:|
|n: 9.<br>identificadores: 74, 29, 28,86, 46, 43, 33, 32, 28.|Erro: esse identificador já foi usado.Insira outro:|
|n: 10. identificadores: 19, 76, 57,71, 41, 27, 91, 72, 93, 1.<br> meses: 0, 49, 51, 53, 96, 55, 33, 88, 6, 58.Erro: os meses devem ser maiores que 0.<br> Insira outro:|
|n: 11.<br>identificadores: 11, 79, 86,67, 23, 84, 7, 96, 6, 42, 33.<br>meses: 21, 44, 44, 31, 88,96, 33, 22, 91, 41, 6.|Erro: esse mês já foi usado. Insira outro:|