# Exercício 32

[**Ver Análise**](Analise32.md)

```markdown
Algoritmo "Q32 - Repeticao"
Var
   lsup, linf, i, p1, p2, s: inteiro
Inicio
   linf <- 1000
   lsup <- 9999
   escreval("Números que possuem a característica: ")
   escreval
   i <- linf

   enquanto (i <= lsup) faca
      p1 <- i div 100
      p2 <- i - p1 * 100
      s <- p1 + p2

      se ((s^2) = i) entao
         escreva(i, ",")
      fimse

      i <- i + 1
   fimenquanto

   escreval
Fimalgoritmo
