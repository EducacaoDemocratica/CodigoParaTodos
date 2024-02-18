# Exercício 29

[**Ver Análise**](Analise29.md)

```markdown
Algoritmo "Q29 - Repeticao"
Var
   n, c, i, aux: inteiro
Inicio
   c <- -1
   aux <- 1
   i <- -1

   escreva("Insira um número: ")
   leia(n)

   se (n = 0) entao
      i <- 1
   senao
      enquanto (c <> 0) faca
         i <- i + 1
         c <- n div aux
         aux <- aux * 10
      fimenquanto
   fimse

   escreval
   escreval("O número", n," tem", i," algarismos.")
Fimalgoritmo
