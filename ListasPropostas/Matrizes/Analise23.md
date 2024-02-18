# Exercício 23

[*Ver Algoritmo*](Algoritmo23.md)

 *Faça um pseudocódigo que receba a matrícula de 10 alunos e preencha
uma matriz com as notas dos 10 alunos em cada uma das 5 provas de até 12
pontos e de cada um dos 4 trabalhos de até 10 pontos. Imprima o aluno e sua
nota final, sendo essa a soma da média das provas e da média dos trabalhos.
Apresente também a matrícula do aluno que obteve a maior nota final e a média
das notas finais.*


**Entrada**

- A matrícula, as notas de cada uma das 5 provas e de cada um dos 4 trabalhos de
cada um dos 10 alunos.

**Saída**

- A nota final de cada aluno, o aluno com a maior nota final e a média das notas
finais

**Restrições**

- não devem ser aceitos números de matrícula repetidos.
- não deve ser aceito nenhuma nota negativa.

**Exemplo**



| Entrada | Saída |
|-|-|
|//matrícula, notas das provas, notas dos trabalhos<BR>aluno 1: 12;<BR>3.7, 8.7, 3.5, 8.4, 5.3;<BR>6, 7, 4.1, 6.8<BR>aluno 2: 23;<BR>3.2, 3.9, 10.4, 1.7, 10.3;<BR>5.8, 2.5, 0.6, 2.5<BR>aluno 3: 20;<BR>6.6, 9.1, 11.9, 3.3, 1.3;<BR>8.2, 3.5, 5.4, 4.7<BR>aluno 4: 190;<BR>4.6, 4.9, 3.9, 10.5, 3.4;<BR>8.7, 8.7, 10, 6.9,<BR>aluno 5: 9;<BR>9.7, 2.7, 5.8, 8.5, 2.6;<BR>4.9, 8.2, 2.8, 4.8|1º aluno: 0012; Final = 11.895.<BR>2º aluno: 0023; Final = 8.75.<BR>3º aluno: 0020; Final = 11.89.<BR>4º aluno: 0190; Final = 14.035.<BR>5º aluno: 0009; Final = 11.035.<BR><BR>Média das notas finais: 11.521.<BR>Aluno com a maior nota final: 0190;<BR>Final = 14.035.|
|aluno 1: 10;<BR>4.4, 1.9, 2.6, 6.1, 10.8;<BR>4.7, 1.9, 1.9, 8.2,<BR>aluno 2: 10;|Erro: Entrada duplicada. Insira outro valor:|
|alun0 1: 90;<BR>4.2, 8.9, 7.1, 4.8, 12.1|Erro: a nota da prova deve estar entre 0 e 12. Insira outro valor:|
|aluno 1: 6;<BR>4.2, 8.9, 0.8, 3.6, 11.3;<BR>3.7, 2.7, 8.1, -0.1;|Erro: a nota do trabalho deve estar entre 0 e 10. Insira outro valor:|