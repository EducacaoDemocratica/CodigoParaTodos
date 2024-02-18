---
# Exercício 08

[**Ver Algoritmo**](Algoritmo08.md)

*Faça um pseudocódigo que armazene em um registro o nome, a idade, a cidade de origem, o sexo, o peso e a altura de 40 alunos de uma turma e informe os nomes dos alunos com IMC acima do valor médio do IMC da turma. O Índice de Massa Corpórea/IMC é obtido pela divisão do peso pelo quadrado da altura.*

**Entrada**
- O nome, a idade, cidade de origem, sexo, altura e o peso de cada um dos 40 alunos.

**Saída**
- Os nomes dos alunos com IMC acima da média da turma.

**Restrições**
- Os campos nome, a cidade de origem e sexo devem ser preenchidos corretamente.
- Os campos idade, altura e peso não devem aceitar valores negativos ou nulos.

**Exemplo**
*Nota: utilizando 5 alunos na entrada.*

| Entrada                                                    | Saída                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------|
| 1º aluno: “João”, 16, “Ipatinga”, “M”, 1.89, 72 <br> 2º aluno: “Alice”, 18, “Timóteo”, “F”, 1.70, 61.5 <br>3º aluno: “Odilon”, 38, “Coronel Fabriciano”, “M”, 1.75, 82.6 <br>4º aluno: “Daniel”, 15, “Coronel Fabriciano”, “M”, 1.62, 73.4 <br>5º aluno: “Carol”, 17, “Ipatinga”, “F”, 1.59, 52| Alunos com IMC acima da média:<br>Nome: Odilon; IMC: 26.97.<br>Nome: Daniel; IMC: 27.97. |
| 1º aluno: “”                                                | Erro: idade inválida. Insira uma idade maior que 0:             |
| 1º aluno: “Maurílio”, 48, “Timóteo”, “A”                    | Erro: valor inválido encontrado. Insira outro valor para o sexo: |
| 1º aluno: “Ana”, 17, “Timóteo”, “S”, 1.52, -54.2             | Erro: altura inválida. Insira uma altura maior que 0:           |
