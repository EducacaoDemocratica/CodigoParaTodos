# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown
Algoritmo "Q15 - Sequencial"
Var
   n, naux, u, d, c, m: inteiro
Inicio
   escreva("Insira um número de 4 algarismos: ")
   leia(n)
   escreval
   naux <- n
   m <- naux div 1000
   naux <- naux - m * 1000
   c <- naux div 100
   naux <- naux - c * 100
   d <- naux div 10
   u <- naux mod 10
   naux <- 0
   naux <- u * 1000 + d * 100 + c * 10 + m
   escreval("Número original:", n, ".")
   escreval("Número invertido:", naux, ".")
Fimalgoritmo

