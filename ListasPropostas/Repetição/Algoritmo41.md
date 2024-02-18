# Exercício 41

[**Ver Análise**](Analise41.md)

```markdown
Algoritmo "Q41 - Repetição"
Var
   n, i, aux1, aux2, aux3: inteiro
Inicio
   aux1 <- -1
   aux2 <- 1
   escreva("Insira um número inteiro positivo: ")
   leia(n)

   enquanto (n <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(n)
   fimenquanto

   escreval

   enquanto (i < n) faca
      aux3 <- aux1 + aux2
      aux1 <- aux2
      aux2 <- aux3
      i <- i + 1
   fimenquanto

   escreval("O", n, "º número da série de Fibonacci é", aux3, ".")
Fimalgoritmo
