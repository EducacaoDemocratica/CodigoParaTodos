# Exercício 51 - Repetição

[**Ver Análise**](Analise51.md)

```markdown
Algoritmo "Q51 - Repeticao"
Var
   n, no, aux, aux2, a, c: inteiro
   t: logico
Inicio
   c <- -1
   aux <- 1
   t <- verdadeiro

   escreva("Insira um número positivo ou nulo: ")
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
   aux2 <- 1

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
      escreval(no," é um valor válido para a base 2.")
   fimse
Fimalgoritmo
