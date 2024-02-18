# Exercício 31

[**Ver Algoritmo**](Algoritmo31.md)

*Faça um pseudocódigo que leia o número correspondente ao mês atual e os dígitos (somente os quatro números) de uma placa de veículo, e através do número finalizador da placa determine a situação de vencimento do IPVA. Por exemplo: quem tem a placa “1389” paga o IPVA em setembro (mês nove).*

**Entrada**
- Mês atual (m) e os dígitos da placa de um veículo (placa).

**Saída**
- A situação de vencimento do IPVA.

**Restrições**
- Ambos os valores devem ser positivos e não nulos.

**Exemplos**

| Entrada              | Saída                        |
| ---------------------| -----------------------------|
| m: 13, placa: 2004   | Erro: o mês informado não existe. |
| m: 11, placa: 10001  | Erro: formato de placa inválida. |
| m: 12, placa: 5582   | O IPVA venceu faz 10 meses.   |
