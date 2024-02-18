# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown
Algoritmo "Q16 - Repeticao"
Var
   x, y, mdc, menor, aux: inteiro
Inicio
   mdc <- -1
   escreva("Insira um número positivo x: ")
   leia(x)
   
   enquanto (x <= 0) faca
      escreva("O número deve ser positivo: ")
      leia(x)
   fimenquanto
   
   escreva("Insira um número positivo y: ")
   leia(y)
   escreval
   
   enquanto ((y = x) ou (y <= 0)) faca
      se (y = x) entao
         escreva("Esse número já foi usado: ")
      fimse
      se (y <= 0) entao
         escreva("O número deve ser positivo: ")
      fimse
      leia(y)
      escreval
   fimenquanto
   
   se(x > y) entao
      menor <- y
   senao
      menor <- x
   fimse
   
   aux <- menor
   
   enquanto (mdc = -1) faca
      se ((y mod aux = 0) e (x mod aux = 0)) entao
         mdc <- aux
      senao
         aux <- aux - 1
      fimse
   fimenquanto
   
   escreval("O MDC de", x," e", y," é", mdc,".")
Fimalgoritmo

//ou também

Algoritmo "Q16 - Repeticao"
Var
   x, xo, y, yo, mdc, i, d, aux: inteiro
Inicio
   i <- 2
   mdc <- 1
   escreva("Insira um número inteiro positivo: ")
   leia(x)
   
   enquanto (x <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(x)
   fimenquanto
   
   escreva("Insira outro número inteiro positivo: ")
   leia(y)
   
   enquanto (y <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(y)
   fimenquanto
   
   xo <- x
   yo <- y
   
   enquanto ((x + y) <> 2) faca
      aux <- 0
      d <- 0
      
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
            se ((y mod i = 0) e (x mod i = 0)) entao
               y <- y div i
               x <- x div i
               mdc <- mdc * i
            senao
               se (y mod i = 0) entao
                  y <- y div i
               fimse
               
               se (x mod i = 0) entao
                  x <- x div i
               fimse
            fimse
         fimse
      senao
         i <- i + 1
      fimse
   fimenquanto
   
   escreval
   escreval("O MDC de", xo," e", yo," é", mdc,".")
Fimalgoritmo
