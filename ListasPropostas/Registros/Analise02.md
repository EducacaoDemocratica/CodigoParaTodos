# Exercício 02

[*Ver Algoritmo*](Algoritmo02.md)

*Faça um pseudocódigo que armazene em um registro os nomes e a nota final de uma turma de 20 alunos em matemática. As notas são distribuídas em 4 bimestres em até 25 pontos por bimestre. Considerando os mesmos critérios de aprovação do exercício anterior, informe:*

*a. a quantidade de alunos aprovados, em recuperação e reprovados;<br>b. a maior nota final obtida no ano;<br>c.os nomes, em ordem crescente, dos alunos que obtiveram a maior nota final no ano;<br>d. as notas médias de cada bimestre;<br>e. a quantidade de alunos que ficaram com notas acima da média por bimestre.*

**Entrada**

- O nome e as 4 notas de matemática dos 20 alunos.

**Saída**

- A quantidade de alunos em cada situação, a maior nota final e os alunos que a obtiveram em ordem crescente, a média de cada bimestre e a quantidade de alunos que ficaram acima da média também em cada bimestre.

**Restrições**

- o campo nome deve ser preenchido corretamente.
 - uma nota bimestral não deve aceitar valores negativos ou nulos nem acima de 25.

 
**Exemplo**
<sub>*Nota:Utilizando 5 alunos na entrada.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|// nome, as 4 notas de matemática<br>aluno 1: “Lucas”;<br>19.2, 20.2, 12.1, 8.1<br>aluno 2: “Ana”;<br>12.1, 3.2, 15, 21,<br>aluno 3: “Maria”;<br>25, 24, 24.9, 25<br>aluno 4: “João”;<br>15.7, 19.6, 14.1, 19.2<br>aluno 5: “Luiz”;<br>12.1, 1.2, 16, 18.3|Quantidade de alunos aprovados: 2.<br>Quantidade de alunos reprovados: 0.<br>Quantidade de alunos em recuperação: 3.<br>Maior nota final: 98.9.<br>Aluno(s) que a conquistaram: Maria.<br>Nota média de cada bimestre:<br>1º bimestre: 16.82; 2 alunos ficaram acima da média.<br>2º bimestre: 13.64; 3 alunos ficaram acima da média.<br>3º bimestre: 16.42; 1 alunos ficaram acima da média.<br>4º bimestre: 18.32; 3 alunos ficaram acima da média.|
|aluno 1:| “ ”Erro: nome inválido. Preencha esse campo corretamente:|
|aluno 1: “Lara”;<br>19.2, -0.0001|Erro: nota inválida. Insira valores de 0 até 25:|
|aluno 1: “Bárbara”;<br>25.0001|Erro: nota inválida. Insira valores de 0 até 25:|