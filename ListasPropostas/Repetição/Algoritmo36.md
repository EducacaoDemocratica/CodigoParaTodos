# Exercício 36

[**Ver Análise**](Analise36.md)

```markdown
Algoritmo "Q36 - Repeticao"
Var
   n, no, ni, aux, aux2, a, c, r: inteiro
Inicio
   c <- -1
   aux <- 1

   escreva(" Insira um número: ")
   leia(n)
   no <- n
   escreval

   enquanto (c <> 0) faca
      c <- n div aux
      aux <- aux * 10
   fimenquanto

   aux <- aux div 100
   aux2 <- 1

   enquanto (aux > 0) faca
      a <- n div aux
      n <- n - a * aux
      aux <- aux div 10
      ni <- ni + (a * aux2)
      aux2 <- aux2 * 10
   fimenquanto

   escreval(" Número original:", no)
   escreval(" Número invertido:", ni)

   r <- no - ni

   escreval
   escreval(" Subtração do original pelo seu inverso:", r)

   se (r <> 0) entao
      escreval
      escreval(r, " é múltiplo de 9 pois sua divisão por 9 (", r, "/9 =", r div 9,") não tem resto.")
      escreval(" É uma divisão exata.")
   fimse
Fimalgoritmo
