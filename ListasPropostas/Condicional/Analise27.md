# Exercício 27

[**Ver Algoritmo**](Algoritmo27.md)

*Um brasileiro, ao viajar para o Chile, deve levar valores em reais e dólares consigo para trocar por pesos chilenos, a moeda corrente, em casas de câmbios do país, pois a cotação dessas moedas não segue um padrão linear, podendo valer a pena realizar a troca em uma outra moeda no Brasil e depois converter para o peso devido à cotação do dia. Faça um pseudocódigo que receba a cotação dessas moedas e a quantidade de dólar e real que o brasileiro carrega para indicar a melhor troca a ser realizada.*

**Entrada**
- Valor do dólar na casa brasileira, valor do dólar na casa chilena, valor do real na casa chilena, quantidade de dólares e de reais.

**Saída**
- Troca mais vantajosa: ou todas as trocas na casa chilena ou a troca do dólar na casa brasileira e depois a troca da quantia em real total na casa chilena.

**Restrições**
- A cotação não pode ser negativa ou nula.
- A quantidade de moedas não pode ser negativa.

**Exemplos**

| Entrada                                             | Saída                                        |
| ----------------------------------------------------| ---------------------------------------------|
| DólarBR: R$5.25<br>DólarCHI: 943.40 pesos.<br>RealCHI: 182.56 pesos.<br><br>Quantidade em real: R$100,00<br>Quantidade em dólar: US$10,00 | É mais vantajoso trocar o dólar em uma casa brasileira e depois trocar os reais na casa chilena. |
| DólarBR: R$5.25<br>DólarCHI: 943.40 pesos.<br>RealCHI: 182.56 pesos.<br><br>Quantidade em real: R$100,00<br>Quantidade em dólar: US$0,00  | A troca pode ser realizada tanto na casa brasileira como na chilena. |
| DólarBR: R$5.25<br>DólarCHI: 0 pesos.<br>RealCHI: 182.56 pesos.<br><br> Quantidade em real: R$100,00<br>Quantidade em dólar: US$0,00 | Erro, valor inválido encontrado.              |
