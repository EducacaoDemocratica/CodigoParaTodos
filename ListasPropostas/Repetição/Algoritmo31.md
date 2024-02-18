# Exercício 31

[**Ver Análise**](Analise31.md)

```markdown
Algoritmo "Q31 - Repeticao"
Var
   n, no, c, i, aux: inteiro
Inicio
   c <- -1
   aux <- 1
   i <- 0
   escreva("Insira um número: ")
   leia(n)
   escreval

   enquanto (c <> 0) faca
      c <- n div aux
      aux <- aux * 10
   fimenquanto

   no <- n
   se (n < 0) entao
      n <- n * -1
   fimse

   aux <- aux div 100
   enquanto (aux > 0) faca
      c <- n div aux
      n <- n - c * aux
      aux <- aux div 10

      se ((c = 2) ou (c = 3) ou (c = 5) ou (c = 7)) entao
         i <- i + 1
      fimse
   fimenquanto

   escreval("O número", no, "tem",
