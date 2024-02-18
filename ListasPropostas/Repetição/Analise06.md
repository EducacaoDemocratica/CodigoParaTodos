# Exercício 06

[**Ver Algoritmo**](Algoritmo06.md)

*Escreva um pseudocódigo que receba as notas das 2 avaliações bimestrais de que valem 10 pontos cada e a nota de 1 avaliação optativa, também de valor igual a 10 pontos, de 40 alunos de uma classe. Caso o aluno não tenha feito alguma dessas avaliações deve ser atribuída a ele a nota zero. A nota média do bimestre é calculada considerando que a prova optativa pode substituir a nota mais baixa entre as 2 primeiras avaliações. Esse pseudocódigo deve informar:*

*a) A média bimestral, em 10 pontos, de cada aluno.* <br>
*b) A quantidade de alunos que conseguiram a maior média do bimestre.* <br>
*c) A quantidade de alunos que conseguiram média bimestral acima de 6 pontos.* <br>
*d) A quantidade de alunos que fizeram a prova optativa.* <br>
*e) A quantidade de alunos que fizeram a prova optativa e conseguiram média bimestral acima de 6 pontos.* <br>

**Entrada:**
- A nota da avaliação 1 (a1), avaliação 2 (a2) e da avaliação optativa (ao).

**Saída:**
- A maior média e quantos alunos a obtiveram.
- O número de alunos que não fizeram a avaliação optativa e tiveram a média maior ou igual a 6.
- O número de alunos que fizeram a prova optativa.
- O número de alunos que fizeram a prova optativa e conseguiram média bimestral acima de 6 pontos.

**Restrições:**
- As notas devem estar entre 0 e 10.

**Exemplo:**
Nota: utilizando 6 alunos.

| Entrada                     | Saída                                    |
| --------------------------- | ---------------------------------------- |
| a1: 10.0, a2: 4.1, ao: 8.1;<br>a1: 3.0, a2: 7.7, ao: 5.0;<br>a1: 2.3, a2: 3.2, ao: 0;<br>a1: 9.2, a2: 8.9, ao: 0;<br>a1: 5.1, a2: 5.1, ao: 5.2;<br>a1: 8.5, a2: 0, ao: 7.2;  | Maior média: 9.05<br>Alunos que tiraram a maior média: 2<br>Alunos que não fizeram a optativa e tiveram a média maior ou igual a 6: 1<br>Alunos que fizeram a avaliação optativa: 4<br>Alunos que fizeram a optativa e tiveram a média maior ou igual a 6: 3 |
| a1: -1, a2: 0, ao: 7.2;       | Não insira uma nota negativa ou maior que 10. |
| a1: 10.1, a2: 5.1, ao: 9.9    | Não insira uma nota negativa ou maior que 10. |
