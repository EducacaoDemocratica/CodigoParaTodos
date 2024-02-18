# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - Repeticao"
Var
   i, n, s, lsup, q: inteiro
   m: real
Inicio
   lsup <- 40
   i <- 0
   q <- 0
   enquanto (i < lsup) faca
      i <- i + 1
      escreva("Insira a", i,"ª idade: ")
      leia(n)
      enquanto (n <= 0) faca
         escreva("Insira uma idade válida (maior que zero): ")
         leia(n)
      fimenquanto
      se (n > 16) entao
         q <- q + 1
      fimse
   fimenquanto
   escreval
   escreval("Existem", q," alunos com idade maior que 16 anos.")
Fimalgoritmo
