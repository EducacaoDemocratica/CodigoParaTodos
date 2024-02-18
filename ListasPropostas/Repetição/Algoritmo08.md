# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - Repeticao"
Var
   aux, n, d, i, q: inteiro
Inicio
   i <- 1
   escreva("Insira um número maior que 1: ")
   leia(n)
   enquanto (n <= 1) faca
      escreva("O número precisa ser maior que 1: ")
      leia(n)
   fimenquanto
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
         q <- q + 1
      fimse
   fimenquanto
   escreval
   escreval("De 1 até", n," existem", q," números primos.")
Fimalgoritmo
