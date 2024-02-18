# Exercício 40

[**Ver Algoritmo**](Algoritmo40.md)

*A conta da energia elétrica é calculada levando em consideração o custo de disponibilidade dos serviços da concessionária, o custo do consumo real do estabelecimento, a taxa fixa de iluminação pública cobrada pelo município, o custo da bandeira vigente e um imposto de 34% sobre o custo do consumo. O custo de disponibilidade dos serviços da concessionária envolve 2 modalidades de custos: A classe de fornecimento de energia e a natureza do estabelecimento consumidor. De modo geral, a classe pode ser: monofásica, bifásica ou trifásica. Para a classe monofásica cobra-se um valor fixo referente a 30 vezes o valor unitário do kWh. Para a classe bifásica cobra-se um valor fixo referente a 50 vezes o valor unitário do kWh. Para a classe trifásica cobra-se um valor fixo referente a 100 vezes o valor unitário do kWh. O parâmetro natureza do estabelecimento consumidor também é dividido por classes, sendo B1 – Residência normal, B2 – Residência Rural, B3 – estabelecimento industrial e o C1 – Residência de baixa renda. Assim para cálculo do valor do custo do consumo real do estabelecimento tem-se que a classe B1 é classe de referência e paga o valor unitário do kWh normal. A classe B2 tem uma diminuição de 30% no custo do valor unitário do kWh, C1 uma diminuição de 65% no custo do valor unitário do kWh e B3 um acréscimo de 25% nesse mesmo custo. (Obs: Esses índices percentuais não são reais.)*

**Entrada:**
- Valor do kWh(k), quantidade de kWh consumidos (c), valor da bandeira (b), taxa de iluminação pública (vtaxa), classe (cl), natureza do estabelecimento (n).

**Saída:**
- Valor da conta de energia elétrica.

**Restrições:**
- Sem valores negativos e nulos para kWh, bandeira, taxa.
- Sem valor negativo para a quantidade consumida.
- Sem valor inválido para a natureza ou classe.

**Exemplos:**

| Entrada | Saída |
| ------- | ----- |
| kWh:1.31, kWh consumidos:0, bandeira:31, iluminação pública: 14, classe:"Monofásica", natureza:"Normal" | Valor total da conta: R$ 53.3 |
| kWh: 0.31; kWh consumidos: 0; bandeira: 1; iluminação pública: 0; classe: "Trifásica"; natureza: "Rural" | Erro: valor inválido para a taxa de iluminação pública |
