# Exercício 12

[*Ver Algoritmo*](Algoritmo12.md)

 *A conta da energia elétrica é calculada levando em consideração alguns custos contratuais, como a disponibilidade dos serviços da concessionária, o consumo real do estabelecimento, a taxa de iluminação pública cobrada pelo município sobre o custo de consumo e o da bandeira vigente, além de um imposto de 34% também sobre o valor pago pela quantidade consumida de energia. A referência para o cálculo dos valores a serem pagos é o valor unitário do consumo de 1 quilowatt-hora/kWh, sempre informado na conta de luz.*

*A disponibilidade da concessionária envolve 2 modalidades de custos: a classe de fornecimento de energia e a natureza do estabelecimento consumidor.*

*A classe de fornecimento de energia pode ser monofásica, bifásica ou trifásica. Para a classe monofásica cobra-se um valor fixo referente a 30 vezes o valor unitário do kWh, para a bifásica cobra-se um valor referente a 50 vezes o valor do kWh, e para a trifásica cobra-se 100 vezes o valor do kWh.*

*A natureza do estabelecimento consumidor também é dividida por classes, sendo B1 – Residência normal, B2 – Residência Rural, B3 – estabelecimento industrial e C1 –Residência de baixa renda. Assim, para o cálculo do valor real a ser pago pelo kWh,tem-se que a classe B1 é a de referência pois paga o valor normal do kWh. A classe B2 tem uma diminuição de 30% e C1 uma diminuição de 65% no valor unitário do kWh, além de não pagar a taxa de iluminação pública. Já a classe B3 tem um acréscimo de 25% nesse mesmo custo.Esses índices percentuais não são reais.*

*Faça um pseudocódigo que receba o valor unitário do kWh, a taxa fixa de iluminação pública cobrada pelo município e o valor da bandeira vigente. Armazene em um registro o nome, a classe de fornecimento de energia, a natureza do estabelecimento consumidor e a quantidade de kWh consumidos de cada um dos 300 clientes de uma pequena cidade. Não se esqueça do imposto cobrado sobre o custo do consumo de kWh.*

*Após o fim da coleta de dados, informe:<br>a.o valor final da conta de cada cliente;<br>b.os nomes dos clientes que possuem o maior valor final de conta;<br>c.o total arrecadado pela concessionária de energia elétrica na região; <br>d.os nomes dos clientes que possuem residência rural;<br>e.a quantidade de clientes que possuem classe de fornecimento bifásica;<br>f.o valor arrecadado pela prefeitura com a taxa de iluminação pública;<br>g.os nomes dos clientes isentos da taxa de iluminação pública;*

**Entrada**

- O valor unitário do kWh, a taxa de iluminação pública e o custo da bandeira vigente. Também o nome, classe de fornecimento, a natureza do estabelecimento e a quantidade de kWh consumidos de cada um dos 300 clientes.

**Saída**

- A impressão dos dados dos 10 voos e dos aeroportos após o fim do dia.

**Restrições**

- o valor do kWh, da taxa de iluminação pública e da bandeira não devem ser negativos ou nulos; 
- o nome deve ser preenchido corretamente;
- não devem ser aceitos nomes repetidos;
- só existem três classes de fornecimento: monofásica, bifásica e trifásica;
- só existem quatro tipos de estabelecimento: B1, B2, B3 e C1;
- a quantidade de kWh consumidos não deve ser negativa.

**Exemplo**

| Entrada | Saída |
|-|-|
|kWh: 0.56<br>iluminação: 5%<br>bandeira: 54.00<br>//nome, fornecimento, estabelecimento, quantidade de kWh consumidos<br>c1: “Lucas”, Bifásico, Normal, 100<br>c2: “Mateus”, Trifásico, Industrial,250<br>c3: “José”, Monofásico, Rural, 40<br>c4: “Maria”, Bifásico, Baixa Renda,50<br>c5: “Pedro”, Bifásico, Normal, 200|1º cliente: LUCAS.<br>Classe: BIFÁSICA.<br>Natureza: RESIDÊNCIA NORMAL.<br>kWh consumidos: 100.<br>Total: R$ 157.04.<br>2º cliente: MATEUS.<br>Classe: TRIFÁSICA.<br>Natureza: ESTABELECIMENTO INDUSTRIAL.<br>kWh consumidos: 250.<br>Total: R$ 344.5.<br>3º cliente: JOSÉ.<br>Classe: MONOFÁSICA.<br>Natureza: RESIDÊNCIA RURAL.<br>kWh consumidos: 40.<br>Total: R$ 91.8112.<br>4º cliente: MARIA.<br>Classe: BIFÁSICA.<br>Natureza: RESIDÊNCIA DE BAIXA RENDA.<br>kWh consumidos: 50.<br>Total: R$ 95.132.<br>5º cliente: PEDRO.<br>Classe: BIFÁSICA.<br>Natureza: RESIDÊNCIA NORMAL.<br>kWh consumidos: 200.<br>Total: R$ 232.08.<br>Maior valor final de conta: R$344.5.<br>Clientes que possuem tal valor:MATEUS.<br>Total arrecadado na região: R$ 920.5632.<br>Clientes que possuem residência rural: JOSÉ.<br>Clientes que possuem classe de fornecimento bifásica: 3.<br> Valor arrecadado com iluminação pública: R$ 17.934.<br>Clientes isentos da taxa de iluminação pública: MARIA.|
|kWh: 0.70<br>iluminação: 11%<br>bandeira: 100.00<br>c1: “André”, Monofásico, Normal,150<br>c2: “Maurílio”, Monofásico, Normal,450<br>3: “Odilon”, Trifásico, Industrial,300<br>c4: “Ana”, Monofásico, Industrial,400<br>c5: “Luiza”, Trifásico, Normal, 70|1º cliente: ANDRE.<br>Classe: MONOFÁSICA.<br>Natureza: RESIDÊNCIA NORMAL.<br>kWh consumidos: 150.<br>Total: R$261.70.<br>2º cliente: MAURÍLIO.<br>Classe: MONOFÁSICA.<br>Natureza: RESIDÊNCIA NORMAL.<br>kWh consumidos: 450.<br>Total: R$543.10.<br>3º cliente: ODILON.<br>Classe: TRIFÁSICA.<br>Natureza: ESTABELECIMENTO INDUSTRIAL.<br>kWh consumidos: 300.<br>Total: R$521.75.<br>4º cliente: ANA.<br>Classe: MONOFÁSICA.<br>Natureza: ESTABELECIMENTO INDUSTRIAL.<br>kWh consumidos: 400.<br>Total: R$590.00.<br>5º cliente: LUIZA.<br>Classe: TRIFÁSICA.<br>Natureza: RESIDÊNCIA NORMAL.<br>kWh consumidos: 70.<br>Total: R$235.66.<br>Maior valor final de conta:<br>R$590.00.<br>Clientes que possuem tal valor: ANA.<br>Total arrecadado na região:R$2152.21.<br>Não houveram clientes que possuem residência rural.<br>Não houveram clientes com classe de fornecimento bifásica.<br>Valor arrecadado com iluminação pública: R$118.97.<br>Não houveram clientes isentos da taxa de iluminação pública.|
