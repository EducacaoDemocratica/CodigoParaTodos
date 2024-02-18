# Exercício 16

[*Ver Algoritmo*](Algoritmo16.md)

*Faça um pseudocódigo que receba a medida de 3 lados e informe se essas retas podem formar um triângulo. Caso possa formar o triângulo, leia os valores de seus três ângulos e classifique-o em retângulo, obtusângulo e acutângulo.*

**Entrada**
- Medidas de três lados l1, l2 e l3 e de três ângulos a1, a2 e a3.

**Saída**
- Se as medidas podem formar um triângulo e qual o tipo formado.

**Restrições**
- A medida de um lado ou ângulo não pode ser negativa ou nula.
- A soma dos ângulos deve ser igual a 180.

**Exemplos**

| Entrada                                | Saída                       |
| --------------------------------------| ---------------------------|
| l1: 2, l2: 3, l3: 5 <br> a1: 90, a2: 60, a3: 30 | Triângulo retângulo |
| l1: 3, l2: 4, l3: 4 <br> a1: 60, a2: 50, a3: 70 | Triângulo acutângulo |
| l1: 5, l2: 5, l3: 5 <br> a1: 120, a2: 30, a3: 31 | Erro: a soma dos ângulos não é igual a 180. |
| l1: 2, l2: 6, l3: 9 <br> a1: 105, a2: 35, a3: 40 | Os lados não podem formar um triângulo |
| l1: 2, l2: 0, l3: 1 <br> a1: 90, a2: 45, a3: 45 | Medida inválida encontrada |

