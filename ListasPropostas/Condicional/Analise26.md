# Exercício 26

[**Ver Algoritmo**](Algoritmo26.md)

*Faça um pseudocódigo que recebe o valor de uma compra e o valor dado pelo cliente para o seu pagamento, ambos valores inteiros, positivos, e informe ao caixa a menor quantidade de cédulas de dinheiro a serem devolvidas ao cliente. Estão disponíveis cédulas de 100, 50, 20, 10, 5 e 1 real.*

**Entrada**
- Valor do produto e valor fornecido no caixa.

**Saída**
- O valor troco e a quantidade de cédulas devolvidas para o cliente, se houver.

**Restrições**
- Sem valor nulo ou negativo.

**Exemplos**

| Entrada                             | Saída                                                 |
| ------------------------------------| ------------------------------------------------------|
| produto: R$123<br>fornecido: R$333  | Troco: R$210<br>Pode ser devolvido em 7 cédulas:<br>2 cédulas de R$100.<br>1 cédula de R$10.  |
| produto: R$136<br>fornecido: R$472  | Troco: R$336<br>Pode ser devolvido em 7 cédulas:<br>3 cédulas de R$100.<br>1 cédula de R$20.<br>1 cédula de R$10.<br>1 cédula de R$5.<br>1 cédula de R$1. |
| produto: R$363<br>fornecido: R$292  | São necessários mais R$71 para realizar a compra.    |
| produto: R$100<br>fornecido: -R$200 | Erro: valor inválido encontrado.                       |
