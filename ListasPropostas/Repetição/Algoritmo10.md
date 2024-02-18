# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown
Algoritmo "Q10 - Repeticao"
Var
   i, lsup, aux, d, x, y: inteiro
Inicio
   lsup <- 100
   i <- 1
   y <- 2
   escreval("Primos gêmeos entre 1 e 100: ")
   escreval
   enquanto (i < lsup) faca
      i <- i + 1
      aux <- 0
      d <- 0
      enquanto (aux < i) faca
         aux <- aux + 1
         se (i mod aux = 0) entao
            d <- d + 1
         fimse
      fimenquanto
      se (d = 2) entao
         x <- y
         y <- i
         se ((y - x) = 2) entao
            escreval(x," e", y,".")
         fimse
      fimse
   fimenquanto
Fimalgoritmo
