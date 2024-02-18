# Exercício 18

[**Ver Algoritmo**](Algoritmo18.md)

*Um triângulo é classificado em função das medidas de seus ângulos internos em retângulo, obtusângulo e acutângulo. Essa classificação pode ser feita também em função das medidas dos lados a, b e c desse triângulo:*
- É retângulo se $$\(a^2 = b^2 + c^2\).$$
- Obtusângulo se $$\(a^2 > b^2 + c^2\);$$
- Acutângulo se $$\(a^2 < b^2 + c^2\);$$

*Faça um pseudocódigo que receba a medida de 3 lados (a, b e c) e informe se esses lados podem formar um triângulo. Caso possa formar o triângulo, classifique-o considerando as medidas de seus lados.*

**Entrada:**
- Medidas dos lados a, b e c.

**Saída:**
- Tipo de triângulo formado.

**Restrições:**
- Sem medidas nulas ou negativas.

**Exemplos:**

| Entrada        | Saída               |
| ---------------| ------------------- |
| \(a: 10, b: 5, c: 8\) | Obtusângulo |
| \(a: 5, b: 3, c: 4\) | Retângulo |
| \(a: 10, b: 9, c: 8\) | Acutângulo |
| \(a: 0, b: 1, c: 3\) | Valor inválido |
