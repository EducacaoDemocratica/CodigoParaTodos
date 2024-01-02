---
# Exercício 12

*Faça um pseudocódigo que receba a medida de 3 lados de um triângulo e informe se essas retas podem formar um triângulo. Caso possam, suponha que o triângulo seja retângulo e indique qual o lado é a hipotenusa.*

**Entrada**

- Medidas de três lados \(l1\), \(l2\) e \(l3\).

**Saída**

- Se os lados podem formar um triângulo e o valor da hipotenusa do mesmo.

**Restrições**

- A medida de um lado não pode ser negativa ou nula.
- As medidas devem ser diferentes entre si.

**Exemplos**

| Entrada             | Saída                                        |
|---------------------|----------------------------------------------|
| l1: 2; l2: 3; l3: 5 | Os lados podem formar um triângulo. A hipotenusa é o 3º lado com medida 5. |
| l1: 4; l2: 5; l3: 3 | Os lados podem formar um triângulo. A hipotenusa é o 2º lado com medida 5. |
| l1: 9; l2: 7; l3: 9 | Erro: medidas iguais.                        |
| l1: 2; l2: 6; l3: 9 | Os lados não podem formar um triângulo.      |
| l1: 2; l2: 0; l3: 5 | Medida inválida encontrada.                  |

---
