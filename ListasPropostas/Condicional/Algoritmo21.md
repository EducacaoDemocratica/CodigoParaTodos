# Exercício 21

[**Ver Análise**](Analise21.md)

```markdown
Algoritmo "Q21 - Condicional"
Var
   x, y, a, b, c, s, den, d: real
Inicio
   escreva("Insira o valor de x: ")
   leia(x)
   escreva("Insira o valor de y: ")
   leia(y)
   escreva("Insira o valor de a: ")
   leia(a)
   escreva("Insira o valor de b: ")
   leia(b)
   escreva("Insira o valor de c: ")
   leia(c)
   
   s <- (a * x) + (b * y) + c
   den <- ((a^2) + (b^2)) ^ (1/2)

   se (den = 0) entao
      escreval("O somatório é indefinido (divisão por 0).")
   senao
      d <- s / den
      escreval("A distância do ponto (", x, " ,", y, ") à reta s =", s, "é", d, ".")
   fimse
Fimalgoritmo
