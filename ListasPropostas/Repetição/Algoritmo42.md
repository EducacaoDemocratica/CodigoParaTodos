# Exercício 42

[**Ver Análise**](Analise42.md)

```markdown
Algoritmo "Q42 - Repetição"
Var
   n, i, num, den: inteiro
   s: real
Inicio
   i <- 0
   s <- 0
   escreva("Insira um número inteiro positivo: ")
   leia(n)

   enquanto (n <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(n)
   fimenquanto

   escreval

   enquanto (i < n) faca
      i <- i + 1
      num <- (i * 2) - 1
      den <- (i * 2)
      s <- s + (num/den)
   fimenquanto

   escreval("O valor de S é", s, ".")
Fimalgoritmo
