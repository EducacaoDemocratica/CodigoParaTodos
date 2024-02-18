# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown
Algoritmo "Q12 - Sequencial"
Var
   h, m, s, stotal: inteiro
Inicio
   escreva("Insira o valor de horas: ")
   leia(h)
   escreva("Insira os minutos: ")
   leia(m)
   escreva("Insira os segundos: ")
   leia(s)
   escreval
   m <- m + h * 60
   stotal <- s + m * 60
   escreval("Há um total de", stotal, "segundos.")
Fimalgoritmo
