# Exercício 55

[*Ver Algoritmo*](Algoritmo55.md)

*Um contador tem um comportamento muito peculiar. Ele tem dificuldades de fazer contas de cabeça e se atrapalha um pouco com números. Assim ele passa os valores para uma secretária que vai enfileirando os números ditos por ele. Quando o contador erra um número, ele não o corrige, ele apenas fala “zero”. Por exemplo, ao ditar a quantidade vendida de produtos no dia, ele faz assim: 6, 3, 0, 2, 12, 4, 0, 0, 9, 3. A secretária então soma 6 + 2 + 9 + 3. O contador fala até 30 valores por vez, mas não diz quantos vai ditar. Por isso, ele fala um número específico para finalizar a inserção*

*Faça um pseudocódigo que auxilie essa secretária a fazer de forma rápida e segura a soma solicitada por seu chefe.*

**Entrada**

- n números inteiros positivos.

**Saída**

- A soma segura dos valores solicitados pelo chefe.

**Restrições**

- n deve ser maior que 0 e menor/igual a 30.
- os n números não podem ser negativos.
- o número 0 não deve atuar como uma quantidade, mas sim como um indicador de erro.
 
**Exemplo**
*Nota: utilizando -1 como dígito de parada.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|6, 3, 0, 2, 12, 4, 0, 0, 9, 3, -1.|Números após correção: 6, 2, 9, 3.<br>Soma: 20.|
|10, 21, 82, 12, 0, 0, 0, 90,12, 0, -1.|Números após correção: 10, 90.<br>Soma: 100.|
|64, 57, 0, 0, 85, 23, 0, 0, 0|Erro: não existe um valor para ser corrigido. Insira um número diferente de 0.|
|57, 8, 25, 35, 82, 13, 39, 17, 30, -10|Erro: não insira um valor negativo. Insira um número maior/igual a 0:|