# Exercício 35

[**Ver Algoritmo**](Algoritmo35.md)

*Um plano de saúde inovou e criou planos segmentados por idade e por sexo. Assim, o preço da mensalidade para o seu plano de consultas ficou como mostrado na tabela abaixo:*

| Idade        | Homem    | Mulher   |
| ------------ | -------- | -------- |
| 0 a 5        | R$130,00 | R$100,00 |
| 6 a 10       | R$150,00 | R$150,00 |
| 11 a 15      | R$180,00 | R$180,00 |
| 16 a 25      | R$180,00 | R$210,00 |
| 26 a 35      | R$200,00 | R$210,00 |
| Acima de 35  | R$230,00 | R$200,00 |

**Entrada:**
- Sexo e idade do paciente.

**Saída:**
- Mensalidade do plano de saúde.

**Restrições:**
- Sem idades negativas ou nulas.
- Sem entrada inválida para o sexo.

**Exemplos:**

| Entrada                 | Saída |
| ------------------------| ------|
| Sexo: “Feminino”, Idade: 27 | R$210 |
| Sexo: “Masculino”, Idade: 27 | R$200 |
| Sexo: “”, Idade: 18     | Erro: código não encontrado. |
| Sexo: “A”, Idade: 0     | Erro: código não encontrado. |
| Sexo: “Feminino”, Idade: 0 | Erro: idade negativa ou nula encontrada. |
