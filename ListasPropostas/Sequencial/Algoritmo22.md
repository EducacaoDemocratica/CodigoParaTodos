# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown
Algoritmo "Q22 - Sequencial"
Var
   a, b, c, p, area: real
Inicio
   escreva("Insira o valor do lado a: ")
   leia(a)
   escreva("Insira b: ")
   leia(b)
   escreva("Insira c: ")
   leia(c)
   escreval
   p <- (a + b + c)/2
   area <- (p * (p - a) * (p - b) * (p - c)) ^ (1/2)
   escreval("A área do triângulo é", area:6:2, ".")
Fimalgoritmo
