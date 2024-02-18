# Exercício 08

[*Ver Algoritmo*](Algoritmo08.md)

*Faça um pseudocódigo que armazene em um registro o nome de até 15 caracteres, a potência (kW) e o tempo ativo por dia de 5 eletrodomésticos. Leia um número n de dias e apresente o consumo total da casa e o consumo relativo de cada eletrodoméstico (porcentagem em relação ao consumo total) neste período de tempo.*

**Entrada**

- O nome, a potência e a quantidade de horas ativo de cada um dos 5 eletrodomésticos e um número n de dias.

**Saída**

- O consumo total da casa e o consumo relativo de cada eletrodoméstico no período.

**Restrições**

- o nome deve ser preenchido e conter até 15 caracteres.
- não deve ser aceito nenhum valor negativo ou nulo.
- não devem ser aceitos nomes repetidos.
 
**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|/nome, potência, tempo diário<br>e1: “Geladeira”, 55.0, 24<br>e2: “Micro-ondas”, 1.4, 1<br>e3: “Liquidificador”, 4.2, 2<br>e4: “Ventilador”, 2.0, 8<br>e5: “Ar-condicionado”, 5.1, 1<br>n:10 Consumo total da casa: 14232 kWh.<br>Consumo real e relativo de cada eletrodoméstico<br><br>GELADEIRA; 13200 kWh; 92.75%<br>MICRO-ONDAS; 14 kWh; 0.10%<br><br>LIQUIDIFICADOR; 42 kWh; 0.30%<br>VENTILADOR; 160 kWh; 1.12%<br>AR-CONDICIONADO; 816 kWh;5.73%|
|e1: “Air Fryer”, 8.0, 2<br>e2: “ ”|Erro: Nome inválido. Digite novamente:|
|e1: “Torradeira”, 1.0, 1<br>e2: |“Torradeira”Erro: nome inválido. Preencha esse campo corretamente:|
|e1: “Forno”, -1|Erro: potência inválida. Preencha esse campo corretamente:|
|e1: “Purificador de água”, 3, 25|Erro: tempo diário inválido. Preencha esse campo corretamente:|