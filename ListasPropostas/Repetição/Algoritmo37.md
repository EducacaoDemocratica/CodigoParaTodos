# Exercício 37

[**Ver Análise**](Analise37.md)

```markdown
Algoritmo "Q37 - Repeticao"
Var
   n, no, ni, aux, aux2, a, r, ro, ri, s: inteiro
Inicio
   aux <- 100
   escreva("Insira um número: ")
   leia(n)

   enquanto ((n < 100) ou (n > 999)) faca
      escreva("O número precisa ter 3 algarismos. Leia novamente: ")
      leia(n)
      escreval
   fimenquanto

   escreval
   no <- n
   aux2 <- 1

   enquanto (aux > 0) faca
      a <- n div aux
      n <- n - a * aux
      aux <- aux div 10
      ni <- ni + (a * aux2)
      aux2 <- aux2 * 10
   fimenquanto

   escreval("Número original:", no)
   escreval("Número invertido:", ni)
   escreval

   r <- no - ni

   se (r < 0) entao
      r <- r * -1
   fimse

   ro <- r
   aux <- 100
   aux2 <- 1

   enquanto (aux > 0) faca
      a <- r div aux
      r <- r - a * aux
      aux <- aux div 10
      ri <- ri + (a * aux2)
      aux2 <- aux2 * 10
   fimenquanto

   escreval("Resultado original:", ro)
   escreval("Resultado invertido:", ri)
   s <- ro + ri

   escreval
   escreval("Soma final:", s)
   escreval
   escreval("Operações: ")
   escreval
   escreval("|", no, " -", ni, "| =", ro)
   escreval(ro, " +", ri, " =", s)
Fimalgoritmo
