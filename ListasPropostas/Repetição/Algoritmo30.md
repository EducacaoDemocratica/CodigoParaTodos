# Exercício 30

[**Ver Análise**](Analise30.md)

```markdown
Algoritmo "Q30 - Repeticao"
Var
   n, no, c, i, aux: inteiro
Inicio
   c <- -1
   aux <- 1
   i <- 0

   escreva("Insira um número: ")
   leia(n)
   escreval

   se (n = 0) entao
      i <- 1
   senao
      enquanto (c <> 0) faca
         c <- n div aux
         aux <- aux * 10
      fimenquanto

      no <- n
      aux <- aux div 100

      enquanto (aux > 0) faca
         c <- n div aux
         n <- n - c * aux
         aux <- aux div 10
         se (c mod 2 = 0) entao
            i <- i + 1
         fimse
      fimenquanto
   fimse

   escreval("O número", no," tem", i," algarismo(s) par(es).")
Fimalgoritmo
