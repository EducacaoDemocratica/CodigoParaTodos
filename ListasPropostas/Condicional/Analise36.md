# Exercício 36

[**Ver Algoritmo**](Algoritmo36.md)

*Crie um algoritmo que informe a quantidade total de calorias de uma refeição escolhida pelo usuário.*

| Prato       | Calorias |
| ----------- | -------- |
| Vegetariano | 180 cal  |
| Peixe       | 230 cal  |
| Frango      | 250 cal  |
| Carne       | 350 cal  |

| Sobremesa     | Calorias |
| ------------- | -------- |
| Sorvete diet  | 110 cal  |
| Mousse diet   | 170 cal  |
| Mousse de chocolate | 200 cal |

| Bebida         | Calorias |
| -------------- | -------- |
| Chá            | 20 cal   |
| Suco de laranja | 70 cal  |
| Suco de melão  | 100 cal  |
| Refrigerante diet | 65 cal |

**Entrada:**
- O prato, a sobremesa e a bebida escolhidos (p, s e b).

**Saída:**
- Quantidade de calorias consumidas.

**Restrições:**
- Não pode entrar nenhum prato fora do cardápio.

**Exemplos:**

| Entrada                                        | Saída    |
| ----------------------------------------------- | -------- |
| Prato: “nenhum”, Sobremesa: “nenhum”, Bebida: “refrigerante diet” | 100 cal. |
| Prato: “frango”, Sobremesa: “mousse de chocolate”, Bebida: “cerveja” | Erro: valor inválido encontrado. |
