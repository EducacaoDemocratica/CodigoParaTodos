# Exercício 26

[**Ver Análise**](Analise26.md)

```markdown
Algoritmo "Q26 - Repeticao"
Var
   n2, i, p: inteiro
   n1: real
Inicio
   p <- 1
   i <- 0
   escreva("Insira um número positivo: ")
   leia(n1)
   
   enquanto (n1 < 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n1)
      escreval
   fimenquanto
   
   escreva("Insira um número positivo: ")
   leia(n2)
   
   enquanto (n2 < 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n2)
      escreval
   fimenquanto
   
   escreval
   escreva("Exponenciação da base", n1," elevada a", n2,":")
   escreval
   
   enquanto (i < n2) faca
      i <- i + 1
      se (i = n2) entao
         escreva(n1," =")
      senao
         escreva(n1," *")
      fimse
      p <- p * n1
   fimenquanto
   
   escreval(p)
Fimalgoritmo
