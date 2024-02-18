# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - Repeticao"
Var
i, n, menor, lsup, qtMenor: inteiro
Inicio
   lsup <- 40
   i <- 0
   qtMenor <- 0
   enquanto (i < lsup) faca
      i <- i + 1
      escreva("Insira a", i,"ª idade: ")
      leia(n)
      enquanto (n <= 0) faca
         escreva("Insira uma idade válida (maior que zero): ")
         leia(n)
      fimenquanto
      se (i = 1) entao
         menor <- n
      senao
         se (n < menor) entao
            qtMenor <- 0
            menor <- n
         fimse
      fimse
      se (n = menor) entao
         qtMenor <- qtMenor + 1
      fimse
   fimenquanto
   escreval
   escreval("A menor idade da turma é", menor," ano(s) e", qtMenor, "estudante(s) a tem.")
Fimalgoritmo
