# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown
Algoritmo "Q18 - Repeticao"
Var
   n, no, p, aux, i, d: inteiro
Inicio
   p <- 1
   i <- 1
   
   escreva("Insira um número maior que 1: ")
   leia(n)
   
   enquanto (n <= 1) faca
      escreva("O número deve ser maior que 1: ")
      leia(n)
      escreval
   fimenquanto
   
   no <- n
   escreval
   escreva(no, " é produto da multiplicação: 1 x")
   
   enquanto (i < n) faca
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
         enquanto (n mod i = 0) faca
            p <- p * i
            n <- n div i
            
            se (p = no) entao
               escreval(i,".")
            senao
               escreva(i," x")
            fimse
         fimenquanto
      fimse
   fimenquanto
Fimalgoritmo
