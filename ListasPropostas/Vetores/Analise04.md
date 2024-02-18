# Exercício 04

[*Ver Algoritmo*](Algoritmo04.md)


*Faça um pseudocódigo que leia a altura e o código do sexo de cada um dos 50 estudantes de uma turma. Calcule e imprima:*

*a. A maior e a menor altura da turma;<br>b. A média de altura da turma;<br>c. A média de altura das mulheres;<br>d. As alturas das alunas com altura acima da média feminina;<br>e. A quantidade de estudantes com altura abaixo da média da turma.*

**Entrada**
- Altura e sexo dos 50 estudantes de uma turma.

**Saída**
- Maior e menor altura da turma, a média de altura da turma, a média de altura das mulheres, as alturas das mulheres que ficaram acima da média das mulheres e a quantidade de estudantes com altura abaixo da média da turma.

**Restrições**
- A altura deve ser maior que 0.
- Sem entrada inválida para o sexo.

**Exemplo**

| Entrada                                           | Saída                                       |
| ------------------------------------------------- | ------------------------------------------- |
| 1º estudante: 'F', 1.22;<br>2º estudante: 'F', 1.57;<br>3º estudante: 'M', 1.54;<br>4º estudante: 'F', 1.65;<br>5º estudante: 'M', 1.15;<br>6º estudante: 'F', 1.42;<br>7º estudante: 'F', 1.94;<br>8º estudante: 'M', 1.35;<br>9º estudante: 'M', 1.75;<br>10º estudante: 'M', 1.61 | Menor altura da turma 1.22m.<br>Maior altura da turma 1.94m.<br>Média da turma 1.50m.<br>Média das mulheres 1.52m.<br>Altura das mulheres que ficaram acima da média feminina:<br>1.57m.<br>1.65m.<br>1.94m.<br>Altura dos estudantes que ficaram abaixo da média da turma:<br>1.22m.<br>1.15m.<br>1.42m.<br>1.35m. |
| 1º estudante: 'F', 1.16;<br>2º estudante: 'F', 1.9;<br>3º estudante: 'F', 1.53;<br>4º estudante: 'M', 1.82;<br>5º estudante: 'M', 1.1;<br>6º estudante: 'F', 1.95;<br>7º estudante: 'M', 1.42;<br>8º estudante: 'M', 1.24;<br>9º estudante: 'F', 1.69;<br>10º estudante: 'C', 1.48 | Erro: não preencha o campo “sexo” com espaços vazios ou diferentes de 'F'/'M'. Insira outro caractere: |
| 1º estudante: 'M', -0.21;<br>2º estudante: 'F', 1.68;<br>3º estudante: 'F', 1.90;<br>4º estudante: 'M', 1.09; | Erro: a altura deve ser maior que entre 0. Insira outra altura: |
