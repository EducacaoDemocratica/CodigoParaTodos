# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown
Algoritmo "Q13 - Sequencial"
Var
   h, m, s, stotal: inteiro
Inicio
   escreva("Insira a quantidade de segundos: ")
   leia(stotal)
   escreval
   h <- stotal div 3600
   stotal <- stotal - h * 3600
   m <- stotal div 60
   s <- stotal - m * 60
   escreval("Horário no formato hora, minutos, segundos = ", h, ":", m, ":", s, ".")
Fimalgoritmo
