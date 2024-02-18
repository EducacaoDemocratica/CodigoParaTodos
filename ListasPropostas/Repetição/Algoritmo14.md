# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown
Algoritmo "Q14 - Repeticao"
Var
   x, xo, y, yo, mmc, i, d, aux: inteiro
Inicio
   i <- 2
   mmc <- 1
   escreva("Insira um número inteiro positivo: ")
   leia(x)
   
   enquanto (x <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(x)
   fimenquanto
   
   escreva("Insira outro número inteiro positivo: ")
   leia(y)
   
   enquanto (y <= 0) faca
      escreval
      se (y <= 0) entao
         escreva("O número deve ser maior que zero: ")
      fimse
      leia(y)
   fimenquanto
   
   xo <- x
   yo <- y
   
   enquanto ((x + aux <- 0 d <- 0 y) <> 2) faca
      enquanto (aux < i) faca
         aux <- aux + 1
         se (i mod aux = 0) entao
            d <- d + 1
         fimse
      fimenquanto
      
      se (d = 2) entao
         se ((nao(y mod i = 0)) e (nao(x mod i = 0))) entao
            i <- i + 1
         senao
            se (y mod i = 0) entao
               y <- y div i
            fimse
            se (x mod i = 0) entao
               x <- x div i
            fimse
            mmc <- mmc * i
         fimse
      senao
         i <- i + 1
      fimse
   fimenquanto
   
   escreval
   escreval("O MMC de", xo," e", yo," é", mmc,".")
Fimalgoritmo
