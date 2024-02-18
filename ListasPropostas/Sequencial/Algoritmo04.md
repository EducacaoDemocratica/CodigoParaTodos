# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - Sequencial"
Var
   cot, vreal: real
   qdolar: inteiro
Inicio
   escreva("Insira a cotação atual do dólar: ")
   leia(cot)
   escreva("Insira a quantidade de dólar a ser trocada: ")
   leia(qdolar)
   vreal <- cot * qdolar
   escreval
   escreval("Cotação atual do dólar: US$ 1 = R$", cot, ".")
   escreval("Quantidade de dólares trocados:", qdolar, ".")
   escreval("Valor obtido em real (R$):", vreal:6:2, ".")
Fimalgoritmo
