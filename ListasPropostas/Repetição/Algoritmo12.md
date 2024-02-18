# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown
Algoritmo "Q12 - Repeticao"
Var
   n1, n2, menor, i: inteiro
Inicio
   i <- 1
   escreva("Insira um número inteiro positivo: ")
   leia(n1)
   
   enquanto (n1 <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(n1)
   fimenquanto
   
   escreva("Insira outro número inteiro positivo: ")
   leia(n2)
   
   enquanto ((n2 = n1) ou (n2 <= 0)) faca
      escreval
      
      se (n2 = n1) entao
         escreva("Erro: este número já foi usado. ")
      fimse
      
      se (n2 <= 0) entao
         escreva("O número deve ser maior que zero: ")
      fimse
      
      leia(n2)
   fimenquanto
   
   se (n1 > n2) entao
      menor <- n2
   senao
      menor <- n1
   fimse
   
   escreval
   escreva("Divisores comuns entre", n1," e", n2,": 1")
   
   enquanto (i < menor) faca
      i <- i + 1
      se ((n1 mod i = 0) e (n2 mod i = 0)) entao
         escreva(",", i)
      fimse
      
      se (i = menor) entao
         escreval(".")
      fimse
   fimenquanto
Fimalgoritmo
