# Exercício 02

[**Ver Algoritmo**](Algortimo02.md)

*Uma empresa decidiu reajustar o salário de seus funcionários de acordo
como seguinte critério:*

*-30% de aumento para aqueles que recebem até R$1200,00;<br>-20% de aumento para aqueles que recebem acima de R$1200,00 até
R$2500,00;<BR>-10% de aumento para aqueles que recebem acima de R$2500,00;<br>-bônus de 0,25% por ano de serviço na empresa;
bônus de incentivo à educação de 1% por filho em idade escolar.<BR>*

*Faça um pseudocódigo que utilize módulos e armazene em um registro o nome, os anos trabalhados na empresa, o número de filhos em idade escolar e o salário atual de cada um dos 35 funcionários. Imprima os dados dos funcionários em ordem alfabética de seus nomes junto do seu salário antigo e o salário reajustado.
Faça todos os reajustes adotando o salário antigo, não faça reajustes em cima de um valor já
reajustado!*

**Entrada**

- O nome, os anos na empresa, a quantidade de filhos em idade escolar e o salário
atual de cada um dos 35 funcionários.

**Saída**

- Dados dos funcionários em ordem alfabética dos nomes e o seu salário antigo e o
salário reajustado.

**Restrições**

- o campo nome deve ser preenchido corretamente.
- o campo salário não deve aceitar valores negativos ou nulos.
- os campos tempo e quantidade de filhos não devem aceitar valores negativos.

**Exemplo**

| Entrada | Saída | 
|-|-|
| // nome, anos trabalhados, filhos em idade escolar, salário atual<br>funcionário 1: “João”; 10; 3;2.542,32<br>funcionário 2: “Maria”; 8; 0;3982.90<Br>Funcionário 3: “Pedro”; 0; 2;1698.00<Br>funcionário 4: “Ana”; 15; 1;5.290,00<br.funcionário 5: “Luiza”; 3; 0;3.901,98|DADOS DO 1º FUNCIONÁRIO<br>Nome: Ana.<Br>Anos empregado: 15.<BR>Filhos em idade escolar: 1.<BR>Salário atual: R$ 5290.<BR>Salário novo: R$: 6070.275.<BR><BR>DADOS DO 2º FUNCIONÁRIO<BR>Nome: João.<BR>Anos empregado: 10.<BR>Filhos em idade escolar: 3.<BR>Salário atual: R$ 2542.<BR>Salário novo: R$: 2936.01.<BR><BR>DADOS DO 3º FUNCIONÁRIO<BR>Nome: Luiza.<BR>Anos empregado: 3.<BR>Filhos em idade escolar: 0.<BR>Salário atual: R$ 3901.<BR>Salário novo: R$: 4320.3575.<BR><BR>DADOS DO 4º FUNCIONÁRIO<BR>Nome: Maria.<BR>Anos empregado: 8.<BR>Filhos em idade escolar: 0.<BR>Salário atual: R$ 3982.9.<BR>Salário novo: R$: 4460.848.<BR><BR>DADOS DO 5º FUNCIONÁRIO<BR>Nome: Pedro.<BR>Anos empregado: 0.<BR>Filhos em idade escolar: 2.<BR>Salário atual: R$ 1698.<BR>Salário novo: R$: 2071.56.|
|funcionário 1: “ ”;|Erro: nome inválido. Preencha esse campo corretamente:|
|funcionário 1: “Arthur”; -1|Erro: ano inválido. Insira um valor maior ou igual a 0:|
|funcionário 1: “Natan”; 0; -2;|Erro: número de filhos inválido. Insira um valor maior ou igual a 0:|
|funcionário 1: “José”; 10; 0; 0|Erro: salário inválido. Insira um valor maior que 0:|