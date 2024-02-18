# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown
Algoritmo "Q17 - Repeticao"
Var
   x, y, z, mdc, menor, aux: inteiro
Inicio
   mdc <- 0
   escreva("Insira um número positivo x: ")
   leia(x)
   
   enquanto (x <= 0) faca
      escreva("O número deve ser positivo: ")
      leia(x)
      escreval
   fimenquanto
   
   escreva("Insira um número positivo y: ")
   leia(y)
   
   enquanto ((y = x) ou (y <= 0)) faca
      se (y = x) entao
         escreva("Esse número já foi usado. Insira outro: ")
      fimse
      se (y <= 0) entao
         escreva("O número deve ser positivo: ")
      fimse
      leia(y)
      escreval
   fimenquanto
   
   escreva("Insira um número positivo z: ")
   leia(z)
   
   enquanto (((z = x) ou (z = y)) ou (z <= 0)) faca
      se ((z = x) ou (z = y)) entao
         escreva("Esse número já foi usado. Insira outro: ")
      fimse
      se (z <= 0) entao
         escreva("O número deve ser positivo: ")
      fimse
      leia(z)
      escreval
   fimenquanto
   
   escreval
   
   se ((x > y) e (z > y)) entao
      menor <- y
   senao
      se ((z > x) e (y > x)) entao
         menor <- x
      senao
         menor <- z
      fimse
   fimse
   
   aux <- menor
   
   enquanto (mdc = 0) faca
      se ((y mod aux = 0) e (x mod aux = 0) e (z mod aux = 0)) entao
         mdc <- aux
      senao
         aux <- aux - 1
      fimse
   fimenquanto
   
   escreval("O MDC de", x,",", y," e", z," é", mdc,".")
Fimalgoritmo

//ou também

Algoritmo "Q17 - Repeticao"
Var
   x, xo, y, yo, z, zo, mdc, i, d, aux: inteiro
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
   
   escreva("Insira outro número inteiro positivo: ")
   leia(z)
   
   enquanto (z <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(z)
   fimenquanto
   
   xo <- x
   yo <- y
   zo <- z
   
   enquanto ((x + y + z) <> 3) faca
      aux <- 0
      d <- 0
      
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
            se ((y mod i = 0) e (x mod i = 0) e (z mod i = 0)) entao
               y <- y div i
               x <- x div i
               z <- z div i
               mdc <- mdc * i
            senao
               se (y mod i = 0) entao
                  y <- y div i
               fimse
               
               se (x mod i = 0) entao
                  x <- x div i
               fimse
               
               se (z mod i = 0) entao
                  z <- z div i
               fimse
            fimse
         fimse
      senao
         i <- i + 1
      fimse
   fimenquanto
   
   escreval
   escreval("O MDC de", xo," e", yo," e", zo," é", mdc,".")
Fimalgoritmo
