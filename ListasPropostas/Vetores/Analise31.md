# Exercício 31

[*Ver Algoritmo*](Algoritmo31.md)

*Numa corrida há 10 corredores, de número de inscrição de 1 a 10. Faça um pseudocódigo que leia os valores do número do corredor e o seu respectivo tempo na corrida. O programa deve imprimir a qualificação e o tempo de corrida, do primeiro ao décimo colocado, identificando o número de inscrição do corredor referente a aquela colocação. Suponha que não há tempos iguais.*

**Entrada**

- O número de inscrição e o tempo de cada um dos 10 atletas.

**Saída**

- A qualificação de cada corredor, do 1º ao 10º colocado.

**Restrições**

- os números de inscrição vão de 1 a 10 e não devem se repetir.
- não existem tempos iguais.


**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|números: 5, 9, 2, 1, 8, 6, 4, 7, 3,10.<br>tempos: 66, 86, 64, 9, 36, 12, 14,32, 84, 91.|COLOCAÇÃO:<br>Inscrição: Nº 1 - Tempo 9s.<br>Inscrição: Nº 6 - Tempo 12s.<br>Inscrição: Nº 4 - Tempo 14s.<br>Inscrição: Nº 7 - Tempo 32s.<br>Inscrição: Nº 8 - Tempo 36s.<br>Inscrição: Nº 2 - Tempo 64s.<br>Inscrição: Nº 5 - Tempo 66s.<br>Inscrição: Nº 3 - Tempo 84s.<br>Inscrição: Nº 9 - Tempo 86s.<br>Inscrição: Nº 10 - Tempo 91s.<br>|
|números: 3, 6, 10, 8, 9, 5, 1, 2, 7,11|Erro: os números de inscrição vão de 1 a 10. Insira outro:|
|números: 9, 6, 3, 10, 1, 7, 8, 5, 2,9|Erro: esse número já está cadastrado. Insira outro:|
|números: 9, 5, 1, 6, 10, 8, 7, 3, 2,4.<br>tempos: 35, 56, 91, 81, 84, 1, 58,39, 91, 0.|Erro: o tempo deve ser maior que 0. Insira outro:|
|números: 9, 2, 4, 5, 10, 8, 6, 7, 3,1<br>tempos: 15, 55, 89, 47, 95, 32, 96,16, 10, 15.|Erro: esse tempo já está cadastrado. Insira outro:|

