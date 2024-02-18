# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown
Algoritmo "Q23 - Repeticao"
Var
   n, i, fat: inteiro
Inicio
   i <- 0
   fat <- 1
   escreva("Insira um número positivo: ")
   leia(n)
   
   enquanto (n < 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n)
      escreval
   fimenquanto
   
   escreval
   
   enquanto (i < n) faca
      i <- i + 1
      fat <- fat * i
   fimenquanto
   
   escreval("O fatorial de", n," é", fat,".")
Fimalgoritmo
