# Exercício 34

[*Ver Algoritmo*](Algoritmo34.md)

*Juros é o rendimento que se obtém quando se faz uma transação financeira por um determinado período. Assim, ao comprar um produto parcelado ou fazer um empréstimo bancário, sempre haverá um valor a mais cobrado, os juros. Eles fazem parte da remuneração de quem financia o bem ou o capital adquirido. O total a ser pago de juros em uma transação financeira é calculado por:*

$$\[ J = \frac{C \cdot i \cdot t}{100} \]$$

*Onde:*
- \( J \): total de juros a ser cobrado na transação financeira;
- \( C \): capital, valor real da transação;
- \( i \): taxa de juros a ser cobrada em %;
- \( t \): tempo, geralmente em meses, que irá durar a transação financeira.

**Entrada**
- O capital \( C \) a ser investido, a taxa de juros \( i \) a ser cobrada e o tempo \( t \) da transação.

**Saída**
- O total de juros a ser cobrado.

**Restrições**
- Não insira valores negativos ou nulos.

**Exemplos**

| Entrada | Saída |
| ------- | ----- |
| C: 100000.00 <br> i: 9.8 <br> t: 12 | Valor real da transação: R$100000.00. <br> Taxa de juros aplicada: 9.80%. <br> Tempo de transação: 12 meses. <br> Total de juros cobrado: R$117600.00. <br> Valor total a ser pago: R$217600.00. |
| C: 928.10 <br> i: 18 <br> t: 60 | Valor real da transação: R$928.10. <br> Taxa de juros aplicada: 18.00%. <br> Tempo de transação: 60 meses. <br> Total de juros cobrado: R$10023.48. <br> Valor total a ser pago: R$10951.58. |
