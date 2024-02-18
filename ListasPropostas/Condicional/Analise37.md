# Exercício 37

[**Ver Algoritmo**](Algoritmo37.md)

*Faça um pseudocódigo que receba uma data no formato ddmmaaaa, onde dd é o dia, mm é o mês e aaaa é o ano, e informe se essa data é válida para este século. Por exemplo, 31041985 não é uma data válida, pois o mês 04 tem 30 dias apenas e o ano 1985 não é deste século.*

**Entrada:**
- Uma data (data).

**Saída:**
- Se essa data é válida para este século ou não.

**Restrições:**
- O valor deve ser positivo e estar no formato ddmmaaaa.

**Exemplos:**

| Entrada                 | Saída                    |
| ------------------------| ------------------------|
| 23042003                | Data válida.             |
| 29022004                | Erro: fevereiro tem apenas 28 dias. |
| 21202204                | Erro: o mês 20 não existe.|
