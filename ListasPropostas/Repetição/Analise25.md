# Exercício 25

[**Ver Algoritmo**](Algoritmo25.md)

*A operação de divisão de 2 números positivos, cujos termos recebem o nome de dividendo e divisor respectivamente, pode ser realizada por meio de operações de subtração. Para tanto, basta contar a quantidade de vezes que é possível subtrair o divisor do dividendo, até que o dividendo seja menor que o divisor. Por exemplo, a divisão de 15 por 3 (15/3 = 5).*

- 15 – 3 = 12.
- 12 é menor que 3?
- Se não, uma nova subtração poderá ser realizada.
- 12 – 3 = 9; 9 – 3 = 6; 6 – 3 = 3; 3 – 3 = 0.

*E assim por diante até que o novo dividendo seja menor que o divisor. Como foram feitas 5 subtrações, tem-se que o resultado de 15/3 é igual a 5. Observe que esse método só apresenta o resultado inteiro da divisão.*

**Entrada:**
- Dois números inteiros positivos m e n.

**Saída:**
- A divisão de m por n utilizando somente subtrações e o resto dessa divisão.

**Restrições:**
- n e m precisam ser maiores que zero.

**Exemplo:**

| Entrada | Saída |
| ------- | ----- |
| n: 7, m: 3 | 7-3=4<br>4-3=1<br><br>Resultado inteiro da divisão: 2. Resto da divisão: 1. |
| n: 12, m: 3 |12 - 3 = 9<br>9-3=6<br>6-3=3<br>3-3=0<br><br> Resultado inteiro da divisão: 4. Resto da divisão: 0. |
| n: 43, m: 47 | Resultado inteiro da divisão: 0. Resto da divisão: 43. |
| n: 10, m: 0 | Erro: o número deve ser positivo, leia novamente: |
