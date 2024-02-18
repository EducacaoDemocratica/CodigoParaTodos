# Exercício 21

[*Ver Algoritmo*](Algoritmo21.md)

*Seja um ponto A determinado por sua coordenada cartesiana x e y, A(x, y), e uma reta s determinada por sua equação geral s : ax + by + c = 0, se ambos estiverem num mesmo plano, a distância do ponto A à reta s é dada por:*

$$\[ d = \frac{\left| ax + by + c \right|}{\sqrt{a^2 + b^2}} \]$$

*Faça um pseudocódigo que calcule a distância de um ponto A a uma reta s, sendo dados os valores quaisquer de a, b e c e os valores de x e y.*

**Entrada:**
- Números x, y do ponto A e a, b, c da reta s.

**Saída:**
A distância d entre o ponto A e a reta S.

**Restrições:**
- O resultado de \(a^2 + b^2\) deve ser maior que zero.

**Exemplos:**

| Entrada                  | Saída                     |
| -------------------------| ------------------------- |
| x: 2, y: 8, a: 0, b: 9, c: 10 | 9.111...               |
| x: 3, y: 4, a: 5, b: 10, c: 4 | 5.2771204268995       |
| x: 1, y: 2, a: 0, b: 0, c: -4 | Distância indefinida    |
