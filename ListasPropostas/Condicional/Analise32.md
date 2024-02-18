# Exercício 32

[**Ver Algoritmo**](Algoritmo32.md)

*Escreva um pseudocódigo que leia as notas das 2 avaliações normais e a nota de 1 avaliação optativa. Caso o aluno não tenha feito alguma dessas avaliações deve ser atribuída a nota zero a essa avaliação. Calcule a média do semestre considerando que a prova optativa pode substituir a nota mais baixa entre as 2 primeiras avaliações caso a nota optativa seja maior que a nota mais baixa. Imprima a média e uma mensagem que indique se o aluno foi aprovado (média >= 6), reprovado (média < 4) ou está em recuperação.*

**Entrada**
- As notas das três provas, a1, a2 e ao.

**Saída**
- Média e situação do aluno.

**Restrições**
- O valor mínimo de qualquer prova é 0 e o máximo é 10.

**Exemplos**

| Entrada                    | Saída                         |
| ---------------------------| ------------------------------|
| a1: 9, a2: 10, ao: 8        | Média: 9.5<br>Aprovado        |
| a1: 6, a2: 0, ao: 4         | Média: 5<br>Em recuperação    |
| a1: 4, a2: 1, ao: 3.5       | Média: 3.75<br>Reprovado      |
| a1: 9, a2: 11, ao: 9        | Nota inválida encontrada     |
| a1: 2, a2: -2, ao: 1        | Nota inválida encontrada     |
