# Exercício 39

[**Ver Algoritmo**](Algoritmo39.md)

*Uma instituição de ensino modificou o critério para aprovação de seus estudantes. Pelo novo critério, um único conceito E é suficiente para reprovar um aluno. O aluno pode ter 1 conceito D desde que tenha também pelo menos um conceito A, caso contrário ele estará em recuperação nas disciplinas com esse conceito. Para cada conceito C, o estudante deverá ter um conceito A ou B, em sua avaliação total, assim, as disciplinas com conceito C que ficarem sem um correspondente A ou B, serão colocadas em recuperação. Para os demais casos o estudante estará aprovado.*

**Entrada:**
- Nome e os seis conceitos.

**Saída:**
- Situação final do aluno.

**Restrições:**
- O nome não pode ficar em branco.
- O conceito vai somente de A a E.

**Exemplos:**

| Entrada          | Saída |
| ---------------- | ----- |
| nome: "", c1:"A", c2: "B", c3: "C", c4: "A", c5: "B", c6: "A" | Erro: campo vazio. |
| nome: "Pedro", c1: "A", c2: "B", c3: "D", c4:"A", c5:"B", c6:"E" | Reprovado. |
| nome: "Luiz", c1: "D", c2: "B", c3: "C", c4: "D", c5: "B", c6: "B" | Em recuperação. |
| nome: "André", c1: "C", c2: "A", c3: "B", c4: "B", c5: "B", c6: "A" | Aprovado. |
| nome: "Maria", c1: "A", c2: "B", c3: "C", c4: "D", c5: "E", c6: "F" | Erro: conceito inválido inserido. |
