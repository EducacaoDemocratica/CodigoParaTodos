# Exercício 03

[*Ver Algoritmo*](Algoritmo03.md)

*Uma empresa decidiu reajustar o salário de seus funcionários de acordo como seguinte critério:*<br>
- 30% de aumento para aqueles que recebem até R$1200,00;
- 20% de aumento para aqueles que recebem acima de R$1200,00 até R$2500,00;
- 10% de aumento para aqueles que recebem acima de R$2500,00;
- bônus de 0,25% por ano de serviço na empresa;
- bônus de incentivo à educação de 1% por filho em idade escolar.
*Faça um pseudocódigo que armazene em um registro o nome, os anos trabalhados na empresa, o número de filhos em idade escolar e o salário atual de cada um dos 35 funcionários. Imprima os dados dos funcionários em ordem alfabética de seus nomes junto do seu salário antigo e o salário reajustado.*

**Entrada**

- O nome, os anos na empresa, a quantidade de filhos em idade escolar e o salário atual de cada um dos 35 funcionários.

**Saída**

- Dados dos funcionários em ordem alfabética dos nomes e o seu salário antigo e o salário reajustado

**Restrições**

- o campo nome deve ser preenchido corretamente.
- o campo salário não deve aceitar valores negativos ou nulos.
- os campos tempo e quantidade de filhos não devem aceitar valores negativos.

 
**Exemplo**
<sub>*Nota:Utilizando 5 funcionários na entrada.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|// nome, anos trabalhados, filhos em idade escolar, salário atual<br>funcionário 1: “João”; 10; 3; 2.542,32<br>funcionário 2: “Maria”; 8; 0; 3982.90<br>funcionário 3: “Pedro”; 0; 2;1698.00<br>funcionário 4: “Ana”; 15; 1;5.290,00<br>funcionário 5: “Luiza”; 3; 0;3.901,98|DADOS DO 1º FUNCIONÁRIO<br>Nome: Ana.<br>Anos empregado: 15.<br>Filhos em idade escolar: 1.<br>Salário atual: R$ 5290.<br>Salário novo: R$: 6070.275.DADOS DO 2º FUNCIONÁRIO<br>Nome: João.<br>Anos empregado: 10.<br>Filhos em idade escolar: 3.<br>Salário atual: R$ 2542.<br>Salário novo: R$: 2936.01.<br>DADOS DO 3º FUNCIONÁRIO<br>Nome: Luiza.<br>Anos empregado: 3.<br>Filhos em idade escolar: 0.<br>Salário atual: R$ 3901.<br>Salário novo: R$: 4320.3575<br>DADOS DO 4º FUNCIONÁRIO<br>Nome: Maria.<br>Anos empregado: 8.<br>Filhos em idade escolar: 0.<br>Salário atual: R$ 3982.9.<br>Salário novo: R$: 4460.848.<br>DADOS DO 5º FUNCIONÁRIO<br>Nome: Pedro.<br>Anos empregado: 0.<br>Filhos em idade escolar: 2.<br>Salário atual: R$ 1698.<br>Salário novo: R$: 2071.56.|
|funcionário 1: “ ”;|Erro: nome inválido. Preencha esse campo corretamente:|
|funcionário 1: “Arthur”; -1|Erro: ano inválido. Insira um valor maior ou igual a 0:|
|funcionário 1: “Natan”; 0; -2;|Erro: número de filhos inválido.<br> Insira um valor maior ou igual a 0:|
|funcionário 1: “José”; 10; 0; 0|Erro: salário inválido. Insira um valor maior que 0:|