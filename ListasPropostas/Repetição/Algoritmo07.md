# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - Repeticao"
Var
   aux, n, d: inteiro
Inicio
   aux <- 0
   d <- 0
   escreva("Insira um número maior que 1: ")
   leia(n)
   enquanto (n <= 1) faca
      escreva("O número precisa ser maior que 1: ")
      leia(n)
   fimenquanto
   enquanto (aux < n) faca
      aux <- aux + 1
      se (n mod aux = 0) entao
         d <- d + 1
      fimse
   fimenquanto
   escreval
   se (d = 2) entao
      escreval(n," é primo.")
   senao
      escreval(n," não é primo.")
   fimse
Fimalgoritmo
