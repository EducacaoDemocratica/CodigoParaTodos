# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown
Algoritmo "Q20 - Repeticao"
Var
   linf, lsup, i, s: inteiro
Inicio
   linf <- 1
   i <- 0
   s <- 0
   lsup <- 100
   
   escreval("Os", lsup," primeiros números triangulares: ")
   escreval
   
   enquanto (i < lsup) faca
      i <- i + 1
      s <- s + i
      
      se (i = lsup) entao
         escreva(s,".")
      senao
         escreva(s,",")
      fimse
      
      se (i mod 10 = 0) entao
         escreval
      fimse
   fimenquanto
Fimalgoritmo
