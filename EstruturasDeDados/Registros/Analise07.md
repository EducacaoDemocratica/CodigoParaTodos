---
# Exercício 07

[**Ver Algoritmo**](Algoritmo07.md)

*Faça um pseudocódigo que armazene em um registro o nome, a idade, a cidade de origem, o sexo e a altura de 40 alunos de uma turma e imprima esses dados.*

**Entrada**
- O nome, a idade, cidade de origem, sexo e altura de cada um dos 40 alunos.

**Saída**
- A impressão dos dados da entrada.

**Restrições**
- Os campos nome, cidade de origem e sexo devem ser preenchidos corretamente.
- Os campos idade e altura não devem aceitar valores negativos ou nulos.

**Exemplo**
*Nota: utilizando 5 alunos na entrada.*

| Entrada                                                    | Saída                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------|
| 1º aluno: “Gabriel”, 15, “Ipatinga”, “M”, 1.86<br>2º aluno: “Maria”, 18, “Timóteo”,“F”, 1.72<br>3º aluno: “Arthur”, 17, “Timóteo”, “M”, 1.75<br>4º aluno: “João”, 18, “Coronel Fabriciano”, “M”, 1.78<br>5º aluno: “Ana”, 17, “Timóteo”, “F”,1.59               | DADOS DO 1º ALUNO:<br>Nome: Gabriel.<br>Idade: 15.<br>Cidade de origem: Ipatinga.<br>Sexo: Masculino.<br>Altura: 1.86m.<br>DADOS DO 2º ALUNO:<br>Nome: Maria.<br>Idade: 18.<br>Cidade de origem: Timóteo.<br>Sexo: Feminino.<br>Altura: 1.72m.<br> DADOS DO 3º ALUNO:<br>Nome: Arthur.<br>Idade: 17.<br>Cidade de origem: Timóteo.<br>Sexo: Masculino.<br>Altura: 1.75m.<br> DADOS DO 4º ALUNO:<br>Nome: João.<br>Idade: 18.<br>Cidade de origem: Coronel Fabriciano.<br>Sexo: Masculino.<br>Altura: 1.78m.<br>DADOS DO 5º ALUNO:<br>Nome: Ana.<br>Idade: 17.<br>Cidade de origem: Timóteo.<br>Sexo: Feminino.<br>Altura: 1.59m.|
| 1º aluno: “”                                                | Erro: não preencha com espaços vazios. Insira outro nome:       |
| 1º aluno: Maria, 15, “”                                     | Erro: não preencha com espaços vazios. Insira outra cidade de origem: |
| 1º aluno: José, 18, “Ipatinga”, “A”                         | Erro: valor inválido encontrado. Insira outro valor para o sexo: |
| 1º aluno: Ana, 17, “Timóteo”, “S”, 0                        | Erro: altura inválida. Insira uma altura maior que 0:           |
