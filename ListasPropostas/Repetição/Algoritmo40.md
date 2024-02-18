# Exercício 40

[**Ver Análise**](Analise40.md)

```markdown
Algoritmo "Q40 - Repetição"
Var
   n, i, fat, j, s: inteiro
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
      fat <- 1
      j <- 0

      enquanto (j < i) faca
         j <- j + 1
         fat <- fat * j
      fimenquanto

      s <- s + fat
   fimenquanto

   escreval("O valor de S é", s, ".")
Fimalgoritmo
