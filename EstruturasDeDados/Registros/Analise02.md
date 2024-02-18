---
# Exercício 02

[**Ver Algoritmo**](Algoritmo02.md)

*Faça um pseudocódigo que receba o ano atual e armazene em um registro o nome e a idade de um único aluno, e imprima o nome do aluno e o ano em que ele nasceu. Não considere o mês de nascimento.*

**Entrada**

- O ano atual, o nome e a idade de um aluno.

**Saída**

- A impressão do nome do aluno e seu ano de nascimento.

**Restrições**

- O campo nome deve ser preenchido corretamente.
- O ano e o campo idade não devem aceitar valores negativos ou nulos.
- O ano não pode ser inferior ou igual à idade do aluno.

**Exemplo**

| Entrada          | Saída                                           |
|------------------|-------------------------------------------------|
| nome: “Maria”; <br> idade: 15 <br> ano: 2022| DADOS DO ALUNO(A)<br><br>Nome: Maria <br> Nascimento: 2007|
|nome: “ ”|Erro: não preencha com espaços vazios. Insira outro nome:|
|nome: “João”;<vr>idade: 0|Erro: idade inválida. Insira uma idade maior que 0:|
|nome: “Ana”;<br>idade: 12<br>ano: 0|Erro: ano inválido. Insira um ano maior que 0:|
|nome: “José”; <br>idade: 23<br>ano: 23|Erro: ano inválido. Insira um ano maior que a idade:|