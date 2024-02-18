# Exercício 21

[*Ver Algoritmo*](Algoritmo21.md)

 *Uma clínica realiza exames de rotina em seus pacientes. Cada exame contém o nome do paciente, uma taxa de xolesterol/Xi (número entre 0 e 100), a taxa de broteinas/Bi (número entre -10 e 10) e uma taxa de toroteinas/Ti (um valor entre 50 e 100).*

*Sendo estudos feitos pela clínica, pessoas saudáveis têm valores de Xi entre 30 e 50, Bi entre 3 e 7 e Ti entre 65 e 80. *

*Quando a quantidade de alguma substância é diferente do padrão, o resultado do exame é calculado da seguinte forma:*

- Pacientes com taxa de xolesterol abaixo do normal têm hipoxolesterol e acima do normal possuem hiperxolesterol.
- Pacientes com taxa de broteinas abaixo do normal têm hipobroteina e acima tem hiperbroteina.
- Pacientes com taxa de toroteinas abaixo do normal têm hipotoroteinas e acima do normal hipertoroteinas.
- Ao apresentar uma doença, o estado do paciente é moderado. Duas doenças geram um estado grave e três um estado gravíssimo.

*Faça um pseudocódigo que armazene os dados de 10 pacientes, sendo o nome, a taxa de xolesterol, broteinas e toroteinas, e imprima o resultado de seus exames e o seu estado de saúde.*


**Entrada**

- O nome, taxa de Xi, Bi e Ti de cada um dos 10 pacientes.

**Saída**

- O resultado dos exames e o estado de saúde.

**Restrições**

- o nome não deve estar vazio.
- não devem ser aceitos nomes repetidos.
- o nível de cada substância deve respeitar o limite previsto no enunciado.

**Exemplo**
<sub>Nota: utilizando 5 pacientes na entrada.


| Entrada | Saída |
|-|-|
|paciente 1: “Maria,” 47.7, 0.2, 50.7 <br>paciente 2: “João”, 57.2, 0.1, 55.6 <BR>paciente 3: “José”, 95.3, 8.5, 91.7 <BR>paciente 4: “Maurílio”, 1.2, 6.2, 76<BR>paciente 5: “Odilon”, 45.5, 4, 79.2<BR>|Paciente: MARIA.<BR>Xolesterol: NORMAL<BR>Broteínas: HIPOBROTEÍNA.<BR>Toroteínas: HIPOTOROTEÍNA.<BR>Estado de saúde: GRAVE.<BR> Paciente: JOÃO.<BR>Xolesterol: HIPERXOLESTEROL.<BR>Broteínas: HIPOBROTEÍNA.<BR>Toroteínas: HIPOTOROTEÍNA.<BR>Estado de saúde: GRAVÍSSIMO.<BR>Paciente: JOSÉ.<BR>Xolesterol: HIPEROXOLESTEROL.<BR>Broteínas: HIPERBROTEÍNA.<BR>Toroteínas: HIPERTOROTEÍNA.<BR>Estado de saúde: GRAVÍSSIMO.<BR>Paciente: MAURÍLIO.<BR>Xolesterol: HIPOXOLESTEROL.<BR>Broteínas: NORMAL.<BR>Toroteínas: NORMAL.<BR>Estado de saúde: MODERADO.<BR>Paciente: ODILON.<BR>Xolesterol: NORMAL.<BR>Broteínas: NORMAL.<BR>Toroteínas: NORMAL.<BR>Estado de saúde: SAUDÁVEL.|
|paciente 1: “Lucas”, 30.1, 4.5, 80<br>paciente 2: “Lucas”, 20.7, 7, 55.3|Erro: esse nome já está cadastrado.Insira outro:|
|paciente 1: “”|Erro: preencha esse campo.|
|paciente 1: “Pedro”, -0.1|Erro: a taxa de Xi deve estar entre 0 e 100|
|paciente 1: “Augusto”, 50, -11|Erro: a taxa de Bi deve estar entre -10 e 10:|
|paciente 1: “André”, 47.2, 7, 49|Erro: a taxa de Ti deve estar entre 50 e 100:|