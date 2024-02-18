---
# Exercício 10

[**Ver Algoritmo**](Algoritmo10.md)

*Faça um pseudocódigo que armazene em um registro o nome, a idade e a cidade de origem de 40 alunos de uma turma e imprima os dados por ordem alfabética dos nomes das cidades e em cada cidade por ordem alfabética dos nomes dos alunos.*

**Entrada**
- O nome, a idade e a cidade de origem de cada um dos 40 alunos.

**Saída**
- A impressão dos dados da entrada por ordem alfabética dos nomes das cidades e em ordem alfabética dos nomes dos alunos por cidade.

**Restrições**
- Os campos nome e cidade de origem devem ser preenchidos corretamente.
- O campo idade não deve aceitar valores negativos ou nulos.

**Exemplo**
*Nota: utilizando 5 alunos na entrada.*

| Entrada                                                    | Saída                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------|
| 1º aluno: “João”, 16, “Ipatinga”1º aluno: “João”, 16, “Ipatinga”<br>2º aluno: “Alice”, 18, “Timóteo”<br>3º aluno: “Odilon”, 38, “Coronel Fabriciano” <br>4º aluno: “Arthur”, 15, “Coronel Fabriciano” <br>5º aluno: “Carol”, 17, “Ipatinga”                            | DADOS DO 1º ALUNO:<br>Cidade de origem: Coronel Fabriciano.<br>Nome: Arthur.<br>Idade: 15. <br><br> DADOS DO 2º ALUNO:<br>Cidade de origem: Coronel Fabriciano.<br>Nome: Odilon.<br>Idade: 38. <br><br> DADOS DO 3º ALUNO:<br>Cidade de origem: Ipatinga.<br>Nome: Carol.<br>Idade: 17.<br><br>DADOS DO 4º ALUNO:<br>Cidade de origem: Ipatinga.<br>Nome: João.<br>Idade: 16.<br><br> DADOS DO 5º ALUNO:<br>Cidade de origem: Timóteo.<br>Nome: Alice.<br>Idade: 18.  |
| 1º aluno: “”, 14,                                           | Erro: não preencha com espaços vazios. Insira outro nome:       |
| 1º aluno: “Maria”, 18, “”                                   | Erro: não preencha com espaços vazios. Insira outra cidade de origem: |
| 1º aluno: “Lucas”, 0                                        | Erro: idade inválida. Insira um valor maior que 0:              |


