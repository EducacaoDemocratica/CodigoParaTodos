# Exercício 11

[*Ver Algoritmo*](Algoritmo11.md)

 *Um de nossos alunos ficou sem energia elétrica devido às chuvas e aproveitou o tempo ocioso para fazer um algoritmo que ordenasse em ordem alfabética os nomes dos colegas à medida que fossem cadastrados. Só que essa ordenação imediata foi feita de uma maneira peculiar, pois ele a fez preservando a ordem de entrada dos dados. Para tanto, ele imaginou usar uma ficha com o nome do aluno e uma variável que guarde a o índice do vetor do nome que vem depois dele. Ele também utilizou uma variável para marcar qual o primeiro índice do vetor em ordem crescente e outra para a próxima posição do último nome que aponta para a posição -1, posição inexistente.*

*Faça um pseudocódigo que implemente esse algoritmo para uma turma de 30 alunos. Considere que não haverá nomes iguais..*

**Entrada**

- O nome de cada um dos 30 alunos.

**Saída**

- A impressão dos dados dos 10 voos e dos aeroportos após o fim do dia.

**Restrições**

- o nome deve ser preenchido corretamente.
- não devem ser aceitos nomes repetidos.
- você não deve alterar a ordem do vetor de registros, você deve marcar a posição que contém o nome seguinte seguindo a ordem alfabética.

**Exemplo**

1ª Entrada: “Carlos”
| 1 | 2 | 3 | 4 | 5 | ... | 30|	
|---|---|---|---|---|-----|---|	
|"Carlos"|					
|-1|

Inicio = 1

2ª Entrada: Patrícia
| 1 | 2 | 3 | 4 | 5 | ... | 30|	
|---|---|---|---|---|-----|---|	
|"Carlos"|"Patrícia	|	
|2| -1|

Início = 1

3ª Entrada: Aldo
| 1 | 2 | 3 | 4 | 5 | ... | 30|	
|---|---|---|---|---|-----|---|	
|"Carlos"|"Patrícia	| "Aldo"|
|2| -1|1|

Início = 3

4ª Entrada: Bárbara
| 1 | 2 | 3 | 4 | 5 | ... | 30|	
|---|---|---|---|---|-----|---|	
|"Carlos"|"Patrícia| "Aldo"|"Bárbara"|
|2| -1|4|1|

Início: 3

5ª Entrada: Mariana
| 1 | 2 | 3 | 4 | 5 | ... | 30|	
|---|---|---|---|---|-----|---|	
|"Carlos"|"Patrícia| "Aldo"|"Bárbara"|"Mariana"|
|5| -1|4|1|2|