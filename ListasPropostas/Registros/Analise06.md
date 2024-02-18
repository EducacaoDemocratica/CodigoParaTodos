# Exercício 06

[*Ver Algoritmo*](Algoritmo06.md)

*Faça um pseudocódigo que armazene em um registro o dia, mês e ano de 2 datas. Imprima o número de dias que decorreram entre as duas.*

**Entrada**

- Um dia, mês e ano de cada uma das duas datas.

**Saída**

- A quantidade de dias entre as duas datas, inclusive os dias de cada uma.

**Restrições**

- os dados da data devem ser válidos.

 
**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|//dia, mês, ano <br>data1: 31, 12, 2022<br>data2: 31, 11, 2023|Dados do compromisso<br>Data: 31 / 12 / 2022.<br>Horário: 23h 59min 59s.<br>Descrição: Feliz ano novo!<br>|
|data1: 32|Erro: dia inválido. Insira valores de 1 a 31:|
|data1: 31, 0|Erro: mês inválido. Insira valores de 1 a 12:|
|data1: 29, 2, 2022|Erro: o ano não é bixesseto. Insira valores de 1 a 28.|
|data1: 31, 4|Erro: esse mês possui apenas 30 dias. Insira valores de 1 a 30|