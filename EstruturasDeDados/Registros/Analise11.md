---
# Exercício 11

[**Ver Algoritmo**](Algoritmo11.md)

*Faça um pseudocódigo que armazene em um registro o nome, sexo, idade e salário de um grupo de 30 funcionários e imprima os nomes de cada funcionário do sexo feminino e depois do sexo masculino, o sexo que possui a maior média salarial.Após tais impressões, dê um aumento de 20% no salário de funcionárias maiores de 30 anos e imprima o valor antes e depois do reajuste*

**Entrada**
- O nome, sexo, idade e o salário de cada um dos 30 funcionários.

**Saída**
- A impressão dos nomes das funcionárias e depois dos funcionários, o sexo que possui maior média salarial e a impressão do salário antes e depois do reajuste para as funcionárias maiores de 30 anos.

**Restrições**
- Os campos nome e sexo de origem devem ser preenchidos corretamente.
- O campo idade e salário não devem aceitar valores negativos ou nulos.

**Exemplo**
*Nota: utilizando 5 funcionários na entrada.*

| Entrada                                                    | Saída                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------|
|// nome, sexo, idade, salário1º funcionário: “João”; “M”; 27; 2.843,50 <br> 2º funcionário: “Alice”; “F”; 30; 2.550,81<br> 3º funcionário: “Maurílio”; “M”; 55; 5.632,00<br>4º funcionário: “Maria”; “F”; 35; 7642,01 <br> 5º funcionário: “Carol”; “F”, 29; 2.221,40                    | DADOS DA  1ª FUNCIONÁRIA:<br><br>Nome: Alice.<br>Idade: 30 anos.<br>Salário: R$2550.00.<br><br>DADOS DA  2ª FUNCIONÁRIA:<br><br>Nome: Maria.<br>Idade: 35 anos.<br> Salário: R$7642.01.<br><br>DADOS DA  3ª FUNCIONÁRIA:<br><br>Nome: Carol.<br>Idade: 29 anos.<br>Salário: R$2221.40.<br><br>DADOS DO 1º FUNCIONÁRIO:<br><br>Nome: João.<br>Idade: 27 anos.<br>Salário: R$2843.00.<br><br>DADOS DO  2º FUNCIONÁRIO:<br><br>Nome: Maurílio.<br>Idade: 55 anos.<br>Salário: R$5632.00.<br><br>Média salarial masculina: R$4237.50.<br>Média salarial feminina: R$4137.80.<br>A maior média salarial é a dos homens.<br><br>Reajustes nos salários das funcionárias maiores que 30 anos:<br><br>Nome: Maria.<br>Idade: 35 anos.<br>Salário antigo: R$7642.01.<br>Salário pós reajuste: R$9170.41.|
| 1º funcionário: “André”; “M”; 27; 2.219.03<br>2º funcionário: “Pedro”; “M”; 21;1,621,90<br>3º funcionário: “Tiago”; “M”; 25; 2.612,00<br>4º funcionário: “Mateus”; “M”; 35; 5642,01<br>5º funcionário: “Lucas”; “M”, 29; 4211,40                                        | Não foram inseridas funcionárias no sistema.<br><br>DADOS DO 1º FUNCIONÁRIO:<br><br>Nome: André.<br>Idade: 27 anos.<br>Salário: R$2219.03.<br><br>DADOS DO 2º FUNCIONÁRIO:<br><br>Nome: Pedro.<br>Idade: 21 anos.<br>Salário: R$1621.90.<br><br>DADOS DO 3º FUNCIONÁRIO:<br><br>Nome: Tiago.<br>Idade: 25 anos.<br>Salário: R$2612.00.<br><br>DADOS DO 4º FUNCIONÁRIO:<br><br>Nome: Mateus.<br>Idade: 35 anos.<br>Salário: R$5642.01.<br>DADOS DO 5º FUNCIONÁRIO:<br><br>Nome: Lucas.<br>Idade: 29 anos.<br>Salário: R$421140.00.<br><br>Média salarial masculina: R$86646.99.<br>Média salarial feminina: R$0.00.<br><br>A maior média salarial é a dos homens   |
| 1º aluno: “Maria”, 18, “”                                   | Erro: não preencha com espaços vazios. Insira outra cidade de origem: |
| 1º aluno: “Lucas”, 0                                        | Erro: idade inválida. Insira um valor maior que 0:              |


