# Exercício 07

[*Ver Algoritmo*](Algoritmo07.md)

*Faça um pseudocódigo que crie um registro de horário, composto de hora,minutos e segundos e outro registro de data, composto de dia, mês e ano. Após a criação, “faça” um compromisso composto por uma data, horário e texto que descreve o acontecimento. Imprima o compromisso registrado.*

**Entrada**

- Um texto do acontecimento, uma hora, minuto e segundo, um dia, mês e ano.

**Saída**

- A impressão do compromisso criado.

**Restrições**

- o texto deve ser preenchido corretamente.
- os dados do horário e da data devem ser válidos.
 
**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|hora: 23<br>minuto: 59<br>segundo: 59<br>dia: 31<br>mês: 12<br>ano: 2022<br>texto: “Feliz ano novo!”|Dados do compromisso<br>Data: 31 / 12 / 2022.<br>Horário: 23h 59min 59s.<br:>Descrição: Feliz ano novo!|
|hora: 24|Erro: hora inválida. Insira valores de 0 a 23:|
|hora: 12<br>minuto: 60|Erro: minuto inválido. Insira valores de 0 a 59|
|hora: 12<br>minuto: 0<br>segundo: 0<br>dia: 32|Erro: dia inválido. Insira valores de 1 a 31:|
|hora: 14<br>minuto: 16<br>segundo: 12<br>dia: 31<br>mês: 0|Erro: mês inválido. Insira valores de 1 a 12:|
|hora: 20<br>minuto: 0<br>segundo: 0<br>dia: 29<br>mês: 2<br>ano: 2022|Erro: o ano não é bixesseto. Insira valores de 1 a 28.|
|hora: 19<br>minuto: 30<br>segundo: 0<br>dia: 31<br>mês: 4|Erro: esse mês possui apenas 30 dias. Insira valores de 1 a 30:|