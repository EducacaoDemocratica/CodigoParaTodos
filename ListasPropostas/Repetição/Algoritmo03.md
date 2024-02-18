# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown
Algoritmo "Q3 - Repeticao"
Var
   i, n, s, lsup: inteiro
   m: real
Inicio
   lsup <- 40
   i <- 0
   s <- 0
   enquanto (i < lsup) faca
      i <- i + 1
      escreva("Insira a", i,"ª idade: ")
      leia(n)
      enquanto (n <= 0) faca
         escreva("Insira uma idade válida (maior que zero): ")
         leia(n)
      fimenquanto
      s <- s + n
   fimenquanto
   m <- s/i
   escreval
   escreval("A média de idade da turma é de", m:6:2," anos.")
Fimalgoritmo
