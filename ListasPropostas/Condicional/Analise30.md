# Exercício 30

[**Ver Algoritmo**](Algoritmo30.md)

*Dadas as fórmulas:*
- Peso ideal do homem = (72,7 x altura) – 58;
- Peso ideal da mulher = (62,1 x altura) - 44,7.

*Faça um pseudocódigo que calcule o peso ideal de uma pessoa recebendo a sua altura e o seu sexo.*

**Entrada**
- Altura (h) e sexo (s).

**Saída**
- Peso ideal em kg.

**Restrições**
- A altura deve ser maior que 0.
- Sem entrada inválida para o sexo.

**Exemplos**

| Entrada                  | Saída      |
| -------------------------| -----------|
| h: -2.00, s: “M”         | Altura inválida. |
| h: 1.89, s: “A”          | Código de sexo não encontrado. |
| h: 1.78, s: “F”          | O peso ideal é 65.83kg. |
