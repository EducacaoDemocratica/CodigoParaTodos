# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - Repeticao"
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
   
            menor <- n
         fimse
      fimse
      
   fimenquanto
   escreval
   escreval("A menor idade da turma é", menor," anos.")
Fimalgoritmo
