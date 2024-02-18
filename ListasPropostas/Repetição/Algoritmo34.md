# Exercício 34

[**Ver Análise**](Analise34.md)

```markdown
Algoritmo "Q34 - Repeticao"
Var
   a, a2, a3, b, b2, b3, aux1, aux2, aux3, aux4, aux5, c, i1, i2, achou, j, k, i: inteiro
Inicio
   escreva("Insira um número positivo: ")
   leia(a)

   enquanto (a <= 0) faca
      escreva("O número deve ser positivo: ")
      leia(a)
   fimenquanto

   escreva("Insira um número positivo: ")
   leia(b)

   enquanto (b <= 0) faca
      escreva("O número deve ser positivo: ")
      leia(b)
   fimenquanto

   c <- -1
   aux1 <- 1
   aux2 <- 1
   i1 <- -1
   i2 <- -1

   enquanto (c <> 0) faca
      i1 <- i1 + 1
      c <- a div aux1
      aux1 <- aux1 * 10
   fimenquanto

   aux1 <- aux1 div 100
   c <- -1

   enquanto (c <> 0) faca
      i2 <- i2 + 1
      c <- b div aux2
      aux2 <- aux2 * 10
   fimenquanto

   aux2 <- aux2 div 100
   aux3 <- aux2
   b2 <- b
   j <- b div aux2
   escreval

   escreva("Interseção dos algarismos de", a, " com", b, ":")

   b2 <- b
   a2 <- a
   aux3 <- aux2
   aux5 <- aux1

   enquanto (aux1 > 0) faca
      achou <- 0
      a3 <- a div (aux1 * 10)
      j <- a2 div aux1
      a2 <- a2 - j * aux1
      aux1 <- aux1 div 10
      aux2 <- aux3
      b2 <- b

      enquanto (aux2 > 0) faca
         k <- b2 div aux2
         b2 <- b2 - k * aux2
         aux2 <- aux2 div 10

         se (j = k) entao
            achou <- 1
         fimse
      fimenquanto

      aux4 <- aux5 div 10

      enquanto (aux4 > 0) faca
         k <- a3 div aux4
         a3 <- a3 - k * aux4
         aux4 <- aux4 div 10

         se ((j = k) e (aux4 <> aux1)) entao
            achou <- 1
         fimse
      fimenquanto

      se (achou = 1) entao
         escreva(j, ",")
      fimse
   fimenquanto

   escreval
Fimalgoritmo
