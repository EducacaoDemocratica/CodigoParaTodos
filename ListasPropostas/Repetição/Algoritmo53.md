# Exercício 53 - Repeticao

[**Ver Análise**](Analise53.md)

```markdown
Algoritmo "Q53 - Repeticao"
Var
   n, no, aux, aux2, aux3, a, c, i, bin, k, m, b10: inteiro
   t: logico
Inicio
   c <- -1
   aux <- 1
   t <- verdadeiro
   i <- -1

   escreva("Insira um número binário: ")
   leia(n)

   enquanto (n < 0) faca
      escreva("Não insira números negativos: ")
      leia(n)
   fimenquanto

   no <- n
   escreval

   enquanto (c <> 0) faca
      c <- n div aux
      aux <- aux * 10
   fimenquanto

   aux <- aux div 100
   aux2 <- aux

   enquanto (aux > 0) faca
      a <- n div aux
      n <- n - a * aux
      aux <- aux div 10

      se ((a <> 0) e (a <> 1)) entao
         t <- falso
      fimse
   fimenquanto

   se (t = falso) entao
      escreval(no," não é um valor válido para a base 2.")
   senao
      n <- no
      aux <- aux2
      aux3 <- 1

      enquanto (aux > 0) faca
         a <- n div aux
         n <- n - a * aux
         aux <- aux div 10
         bin <- bin + (a * aux3)
         aux3 <- aux3 * 10
      fimenquanto

      n <- bin

      enquanto (aux2 > 0) faca
         a <- n div aux2
         n <- n - a * aux2
         i <- i + 1
         k <- i
         m <- 1

         enquanto (k > 0) faca
            m <- m * 2
            k <- k - 1
         fimenquanto

         b10 <- b10 + (m * a)
         aux2 <- aux2 div 10
      fimenquanto

      escreval("Valor na base 2: ", no)
      escreval("Valor na base 10: ", b10)
   fimse
Fimalgoritmo
