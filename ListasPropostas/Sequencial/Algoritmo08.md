# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - Sequencial"
Var
   r, li, lc, ai, ac: real
Inicio
   escreva("Insira o raio do círculo (cm): ")
   leia(r)
   escreval
   li <- r * (2 ^ (1/2))
   lc <- r * 2
   ai <- li ^ 2
   ac <- lc ^ 2
   escreval("Raio:", r, "cm.")
   escreval
   escreval("Lado inscrito:", li, "cm.")
   escreval("Área inscrita:", ai, "cm².")
   escreval
   escreval("Lado circunscrito:", lc, "cm.")
   escreval("Área circunscrita:", ac, "cm².")
Fimalgoritmo
