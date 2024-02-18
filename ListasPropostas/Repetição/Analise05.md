# Exercício 05

[**Ver Algoritmo**](Algoritmo05.md)

*Uma sala de aula tem 40 alunos, faça um pseudocódigo que receba o nome, o sexo e número inteiro positivo escolhido por esse aluno. Esse pseudocódigo deve informar:*

*a) a quantidade de meninos que escolheram números par;* <br>
*b) a quantidade de meninas que escolheram número divisível por 5;* <br>
*c) o nome da primeira pessoa que escolheu o maior número.* <br>

**Entrada:**
- Nome, sexo e o número escolhido de cada um dos 40 alunos.

**Saída:**
- Número de meninos que escolheram um número par.<br>
- Número de meninas que escolheram um múltiplo de cinco.<br>
- Nome da pessoa que escolheu o maior número.<br>

**Restrições:**
- O número escolhido precisa ser positivo, os campos nome e sexo não devem ficar vazios.

**Exemplo:**
Nota: utilizando 6 alunos.

| Entrada                                        | Saída                                             |
| ---------------------------------------------- | ------------------------------------------------- |
| nome: “Maria”, sexo: “F”, número: 20;<br> Nome: “João”, sexo: “M”, número: 12;<br> nome: “Ana”, sexo: “F”, número: 17;<br> nome: “Pedro”, sexo: “M”, número: 20;<br> nome: “Luiza”, sexo: “F”, número: 14;<br> nome: “André”, sexo: “M”, número: 7;<br>    | Meninos que escolheram par: 2                     <br>Meninas que escolheram um múltiplo de 5: 1        <br>Pessoa que escolheu o maior número: “Maria”       <br>Pessoa que escolheu o maior número: “Maria”       <br>|
| nome: “João”, sexo: “”, número: 10;<br>        | Erro: campo obrigatório. Por favor, insira um valor para o sexo. <br>|
| nome: “Maria”, sexo: “F”, número: 0;<br>       | Erro: por favor insira um número maior que zero. <br>|
