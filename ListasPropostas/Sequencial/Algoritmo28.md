# Exercício 28

[**Ver Análise**](Analise28.md)

```markdown
Algoritmo "Q28 - Sequencial"
Var
   r1, r2, re: real
Inicio
   escreva("Insira o valor da resistência de R1 (ohms): ")
   leia(r1)
   escreva("Insira o valor da resistência de R2 (ohms): ")
   leia(r2)
   escreval
   re <- 1/((1/r1) + (1/r2))
   escreval("A resistência equivalente aos dois resistores é", re:6:2, "ohms.")
Fimalgoritmo
