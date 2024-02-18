# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown
Algoritmo "Q14 - Sequencial"
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
   escreval("Número:", n, ".")
   escreval("Casa de milhar:", m, ".")
   escreval("Centena:", c, ".")
   escreval("Dezena:", d, ".")
   escreval("Unidade:", u, ".")
Fimalgoritmo
