# Exercício 22

[*Ver Algoritmo*](Algoritmo22.md)

 *O conjunto de dados de uma escola são armazenados em uma matriz nx4. A
1ª coluna da matriz contém a matrícula do aluno no curso, a 2ª o sexo, a 3ª o
código do curso e na 4ª o Coeficiente de Rendimento, CR. Um grupo empresarial
resolveu premiar a aluna com CR mais alto.
Faça um pseudocódigo que preencha uma matriz com as informações de 10
alunos
e imprima a aluna premiada e seu identificador.*


**Entrada**

- A matrícula no curso (4 dígitos), o sexo (1 dígito), o código de curso (3 dígitos) e o CR (2 dígitos) de cada um dos 10 alunos.

**Saída**

- A aluna premiada e seu identificador (linha correspondente na matriz).

**Restrições**

- não devem ser aceitos números de matrícula e CR repetidos.
- o sexo só possui os valores “Masculino” e “Feminino”.
- não deve ser aceito nenhum valor negativo ou nulo.

**Exemplo**



| Entrada | Saída |
|-|-|
|//matrícula; sexo; curso; CR<BR>aluno 1: 12, 1, 002, 90<BR>aluno 2: 3, 2, 001, 85<BR>aluno 3: 35, 1, 002, 86<BR>aluno 4: 8, 2, 001, 99<BR>aluno 5: 10, 1, 003, 91|A aluna 00100391 possui o maior Coeficiente de Rendimento.<BR>CR = 91.|
|aluno 1: 1, 1, 003, 70<BR>aluno 2: 2, 1, 004, 81<BR>aluno 3: 3, 1, 005, 87<BR>aluno 4: 4, 1, 005, 79<BR>aluno 5: 5, 1, 004, 99|Nenhum dado de alguma aluna foi inserido.|
|aluno 1: 10, 1, 003, 70<BR>aluno 2: 10, 2, 002, 99|Erro: entrada repetida. Insira outro valor:|
|aluno 1: 12, 1, 003, 85<BR>aluno 2: 33, 2, 002, 85|Erro: entrada repetida. Insira outro valor:|
|aluno 1: 10000, 1, 032,85|Erro: limite excedido. Insira outro valor:|
|aluno 1: 4319, 0, 012, 90| Erro: valor inválido. Insira outro valor:|