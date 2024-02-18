# Exercício 38

[**Ver Algoritmo**](Algoritmo38.md)

*Uma instituição de ensino decidiu converter todas as notas dos estudantes em conceitos. Para tanto, foi proposta a seguinte tabela de conversão:*

| Nota            | Conceito |
| --------------- | -------- |
| Abaixo de 4      | E        |
| Entre 4 e 6      | D        |
| Entre 6 e 7,5    | C        |
| Entre 7,5 e 8,5  | B        |
| Acima de 8,5     | A        |

*Faça um pseudocódigo que receba o nome e a nota de um estudante e informe qual o conceito que ele terá nesse novo formato de avaliação.*

**Entrada:**
- Nome e nota do estudante.

**Saída:**
- Conceito.

**Restrições:**
- O nome não pode ficar em branco.
- A nota não pode ser negativa ou maior que 10.

**Exemplos:**

| Entrada          | Saída |
| ---------------- | ----- |
| nome: "", nota: 9| Erro: campo vazio. |
| nome: "Pedro", nota: 8.6 | A |
| nome: "Luiz", nota: 7 | C |
| nome: "André", nota: 10.5 | Erro: nota inválida. |
