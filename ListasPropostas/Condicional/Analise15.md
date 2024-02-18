# Exercício 15

[*Ver Algoritmo*](Algoritmo15.md)

*Faça um pseudocódigo que receba a medida de 3 lados e informe se essas retas podem formar um triângulo. Caso possa formar o triângulo, classifique-o quanto às medidas de seus lados.*

**Entrada**
- Medidas de três lados l1, l2 e l3.

**Saída**
- Se as medidas podem formar um triângulo e qual o tipo formado.

**Restrições**
- A medida de um lado não pode ser negativa ou nula.

**Exemplos**

| Entrada            | Saída                                   |
| ------------------ | ---------------------------------------|
| l1: 2, l2: 3, l3: 5| Os lados formam um triângulo escaleno  |
| l1: 3, l2: 4, l3: 4| Os lados formam um triângulo isósceles |
| l1: 5, l2: 5, l3: 5| Os lados formam um triângulo equilátero|
| l1: 2, l2: 6, l3: 9| Os lados não podem formar um triângulo |
| l1: 2, l2: 0, l3: 1| Medida inválida encontrada              |

