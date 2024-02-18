# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown
Algoritmo "Q15 - Repeticao"
Var
   x, xo, y, yo, z, zo, mmc, i, d, aux: inteiro
Inicio
   i <- 2
   mmc <- 1
   escreva("Insira um número inteiro positivo: ")
   leia(x)
   
   enquanto (x <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(x)
      escreval
   fimenquanto
   
   escreva("Insira outro número inteiro positivo: ")
   leia(y)
   
   enquanto (y <= 0) faca
      se (y <= 0) entao
         escreva("O número deve ser maior que zero: ")
      fimse
      leia(y)
      escreval
   fimenquanto
   
   escreva("Insira um terceiro número inteiro positivo: ")
   leia(z)
   
   enquanto (z <= 0) faca
      se (z <= 0) entao
         escreva("O número deve ser maior que zero: ")
      fimse
      leia(z)
      escreval
   fimenquanto
   
   xo <- x
   yo <- y
   zo <- z
   
   enquanto ((x + aux <- 0 d <- 0 y + z) <> 3) faca
      enquanto (aux < i) faca
         aux <- aux + 1
         se (i mod aux = 0) entao
            d <- d + 1
         fimse
      fimenquanto
      
      se (d = 2) entao
         se ((nao(y mod i = 0)) e (nao(x mod i = 0)) e (nao(z mod i = 0))) entao
            i <- i + 1
         senao
            se (x mod i = 0) entao
               x <- x div i
            fimse
            se (y mod i = 0) entao
               y <- y div i
            fimse
            se (z mod i = 0) entao
               z <- z div i
            fimse
            mmc <- mmc * i
         fimse
      senao
         i <- i + 1
      fimse
   fimenquanto
   
   escreval
   escreval("O MMC de", xo,",", yo," e", zo," é", mmc,".")
Fimalgoritmo
