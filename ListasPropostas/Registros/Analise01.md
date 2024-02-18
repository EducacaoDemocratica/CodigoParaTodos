# Exercício 01

[*Ver Algoritmo*](Algoritmo02.md)

*Faça um pseudocódigo que armazene em um registro o nome e as notas finais bimestrais em matemática, português, física e química de um grupo de 35 alunos. As notas são distribuídas em 4 bimestres em até 25 pontos por bimestre. É aprovado o aluno com nota a partir de 60 pontos, fica em recuperação quem possui menos 60 e até 40 pontos e é reprovado quem tem a nota abaixo de 40 pontos. Sabendo que com apenas uma reprovação em uma matéria um aluno é reprovado e só é aprovado quem possui aprovação em todas as disciplinas, informe:*

*a. Os nomes em ordem alfabética dos alunos e sua nota e situação em cada disciplina (aprovado, em recuperação e reprovado) e a situação final;<br>b. Os nomes dos alunos aprovados por disciplina em ordem alfabética;<br>c. Os nomes dos alunos em recuperação por disciplina em ordem alfabética;*

**Entrada**

- O nome e as 4 notas de cada uma das 4 disciplinas dos 35 alunos.

**Saída**

- A impressão dos nomes dos alunos em ordem alfabética e a sua situação, os alunos aprovados por disciplina em ordem alfabética e os reprovados por disciplina também em ordem alfabética.

**Restrições**

- o campo nome deve ser preenchido corretamente.
 - uma nota bimestral não deve aceitar valores negativos ou nulos nem acima de 25.

 
**Exemplo**
<sub>*Nota:Utilizando 3 alunos na entrada.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|// nome, as 4 notas de matemática, as 4 de português, 4 de física, 4 de química<br>aluno 1: “Mateus”;<br>17.3, 15.2, 14.9, 16.1;<br>24, 25, 23.9, 25;<br>15, 14.2, 16.8, 22.9;<br>14.1, 13, 19.8, 20.1;<br>aluno 2: “Lucas”;<br>18.2, 20.2, 25, 17.6;<br>15.2, 14.5, 13.4, 17.9;<br>17.9, 21.4, 12.1, 18.1;<br>10.3, 19.2, 24.6, 25;<br>aluno 3: “Maria”;<br>19.2, 21, 24, 25;<br>18, 20, 25, 25;<br>15, 20.5, 19.2, 18.1;<br>18.2, 21.5, 19, 20.4;|DADOS DO 1º ALUNO<br>Nome: Lucas<br>Matemática: 81<br>Português: 61<br>Física: 69.5<br>Química: 79.1<br>Situação: APROVADO<br>DADOS DO 2º ALUNO<br>Nome: Maria<br>Matemática: 89.2<br>Português: 88<br>Física: 72.8<br>Química: 79.1<br>Situação: APROVADO<br>DADOS DO 3º ALUNO<br>Nome: Mateus<br>Matemática: 63.5<br>Português: 97.9<br>Física: 68.9<br>Química: 67<br>Situação: APROVADO<br>Aprovados em Matemática:<br>Lucas<br>Maria<br>Mateus<br>Aprovados em Portguês:<br>Lucas<br>Maria<br>Mateus<br>Aprovados em Física:<br>Lucas<br>Maria<br>Mateus<br>Aprovados em Química:<br>Lucas<br>Maria<br>Mateus<br>Recuperação em Matemática:<br>Recuperação em Portguês:<br>Recuperação em Física:<br>Recuperação em Química:|
|aluno 1: “ ”;|Erro: nome inválido. Preencha esse campo corretamente:|
|aluno 1: “Ana”;<br>12.3, 0, -0.001|Erro: nota inválida. Insira valores de 0 até 25:|
|aluno 1: “Luiza”;<br>24.99, 25, 25.001,|Erro: nota inválida. Insira valores de 0 até 25:|