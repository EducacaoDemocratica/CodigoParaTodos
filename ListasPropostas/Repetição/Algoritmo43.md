# Exercício 43

[**Ver Análise**](Analise43.md)

```markdown
Algoritmo "Q43 - Repetição"
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
      
      se (i mod 2 = 0) entao
         s <- s - (num/den)
      senao
         s <- s + (num/den)
      fimse
   fimenquanto

   escreval("O valor de S é", s, ".")
Fimalgoritmo
