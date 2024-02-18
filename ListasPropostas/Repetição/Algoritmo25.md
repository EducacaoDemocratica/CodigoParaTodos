# Exercício 25

[**Ver Análise**](Analise25.md)

```markdown
Algoritmo "Q25 - Repeticao"
Var
   n1, n2, i, d: inteiro
Inicio
   i <- 0
   escreva("Insira um número positivo: ")
   leia(n1)
   
   enquanto (n1 <= 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n1)
      escreval
   fimenquanto
   
   d <- n1
   
   escreva("Insira um número positivo: ")
   leia(n2)
   
   enquanto (n2 <= 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n2)
      escreval
   fimenquanto
   
   escreval
   escreval("Divisão de", n1," por", n2,":")
   escreval
   
   enquanto (d >= n2) faca
      i <- i + 1
      d <- d - n2
      escreval(n1," -", n2," =", d)
      n1 <- n1 - n2
   fimenquanto
   
   escreval
   escreval("Resultado inteiro da divisão:", i)
Fimalgoritmo
