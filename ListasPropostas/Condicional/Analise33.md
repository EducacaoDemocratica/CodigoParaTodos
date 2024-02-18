# Exercício 33

[**Ver Algoritmo**](Algoritmo33.md)

*Um endocrinologista deseja controlar a saúde de seus pacientes e, para isso, utiliza o Índice de Massa Corporal (IMC). Sabendo que o IMC é calculado por meio da seguinte fórmula:*

$$IMC = \frac{Peso}{Altura^2}$$

*Onde:*
- *O peso é dado em Kg;*
- *A altura é dada em metros.*

*Elabore um pseudocódigo que leia o nome, o peso e a altura de um paciente, e apresente o nome do paciente e sua faixa de risco, baseando-se na seguinte tabela:*

| IMC                   | Faixa de risco       |
| --------------------- | -------------------- |
| Abaixo de 20          | Abaixo do peso       |
| A partir de 20 até 25 | Normal               |
| Acima de 25 até 30    | Excesso de peso      |
| Acima de 30 até 35    | Obesidade            |
| Acima de 35           | Obesidade Mórbida    |

**Entrada:**
- Nome, peso e altura de um paciente.

**Saída:**
- IMC e faixa de risco.

**Restrições:**
- O nome não pode ficar em branco.
- Sem valor nulo ou negativo.

**Exemplos:**

| Entrada                            | Saída                               |
| -----------------------------------| ------------------------------------|
| nome: “João”, altura: 1.78, peso: 62.5 | IMC: 19.7,<br>Situação: abaixo do peso |
| nome: “”, altura: 1.60, peso: 72.9   | Erro: campo vazio.                  |
| nome: “Ana”, altura: 0, peso: 54.1   | Erro: valor inválido.               |
