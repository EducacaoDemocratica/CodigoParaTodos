# Exercício 52 - Repeticao

[**Ver Análise**](Analise52.md)

```markdown
Algoritmo "Q52 - Repeticao"
Var
   b10, dec, b2, bin, c, i, aux1, aux2, a: inteiro
Inicio
   b2 <- 0
   bin <- 0
   i <- 0
   aux1 <- 1
   aux2 <- 1

   escreva("Insira um número positivo: ")
   leia(b10)

   enquanto (b10 < 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(b10)
   fimenquanto

   escreval

   dec <- b10

   enquanto (b10 > 0) faca
      i <- i + 1
      c <- b10 mod 2
      b10 <- b10 div 2
      b2 <- b2 * 10 + c
   fimenquanto

   enquanto (i > 1) faca
      aux1 <- aux1 * 10
      i <- i - 1
   fimenquanto

   enquanto (aux1 > 0) faca
      a <- b2 div aux1
      b2 <- b2 - a * aux1
      aux1 <- aux1 div 10
      bin <- bin + (a * aux2)
      aux2 <- aux2 * 10
   fimenquanto

   escreval("Número na base 10:", dec)
   escreval("Número na base 2:", bin)
Fimalgoritmo
