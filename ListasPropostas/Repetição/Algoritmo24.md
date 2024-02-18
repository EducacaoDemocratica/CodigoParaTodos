# Exercício 24

[**Ver Análise**](Analise24.md)

```markdown
Algoritmo "Q24 - Repeticao"
Var
   n1, n2, i, m: inteiro
Inicio
   i <- 0
   m <- 0
   escreva("Insira um número positivo: ")
   leia(n1)
   
   enquanto (n1 <= 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n1)
      escreval
   fimenquanto
   
   escreva("Insira um número positivo: ")
   leia(n2)
   
   enquanto (n2 <= 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n2)
      escreval
   fimenquanto
   
   escreval
   
   escreva("Produto de", n1," por", n2,":")
   
   enquanto (i < n2) faca
      i <- i + 1
      se (i = n2) entao
         escreva(n1," =")
      senao
         escreva(n1," +")
      fimse
      m <- m + n1
   fimenquanto
   
   escreval(m)
Fimalgoritmo
