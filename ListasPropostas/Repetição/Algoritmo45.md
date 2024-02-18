# Exercício 45

[**Ver Análise**](Analise45.md)

```markdown
Algoritmo "Q44 - Repeticao"
Var
   i, n, k, lsup: inteiro
   fat, num, x, cosx: real
Inicio
   lsup <- 15
   escreva("Insira o valor de xº: ")
   leia(x)
   
   enquanto ((x < 0) ou (x > pi/2)) faca
      escreva("x deve ser maior/igual a zero e menor/igual a 1.57: ")
      leia(n)
   fimenquanto

   n <- -2
   para i de 1 ate lsup faca
      n <- n + 2
      num <- x ^ n
      k <- 0
      fat <- 1
      
      enquanto (k < n) faca
         k <- k + 1
         fat <- fat * k
      fimenquanto
      
      se (i mod 2 = 0) entao
         cosx <- cosx - num/fat
      senao
         cosx <- cosx + num/fat
      fimse
   fimpara

   escreval
   escreval("O cosseno de", x, " é", cosx:6:2)
Fimalgoritmo
