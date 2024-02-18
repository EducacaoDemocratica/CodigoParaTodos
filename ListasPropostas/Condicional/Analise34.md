# Exercício 34

[**Ver Algoritmo**](Algoritmo34.md)

*Crie um pseudocódigo que, a partir do peso do paciente, calcule a dosagem de determinado medicamento e imprima a receita informando quantas gotas do medicamento o paciente deve tomar por dose. Considere que o medicamento em questão possui 500 mg por ml, e que cada ml corresponde a 10 gotas.*

| Peso        | Dosagem   |
| ----------- | --------- |
| 5 a 9 kg    | 100 mg    |
| 9,1 a 16 kg | 250 mg    |
| 16,1 a 24 kg| 350 mg    |
| 24,1 a 30 kg| 500 mg    |
| Acima de 30 kg | 750 mg  |

**Entrada:**
- Peso do paciente.

**Saída:**
- Dosagem em gotas, mg e ml.

**Restrições:**
- Sem valor nulo ou negativo.

**Exemplos:**

| Entrada | Saída                              |
| --------| -----------------------------------|
| 19.2    | Dosagem: 350mg/ 0.7ml.<br>Gotas: 7. |
| 0       | Erro: peso nulo ou negativo encontrado. |
| 38.5    | Dosagem: 750mg/ 1.5ml.<br>Gotas: 15. |
