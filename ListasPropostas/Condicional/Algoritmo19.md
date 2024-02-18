# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - Condicional"
Var
   x, y, fx: real
Inicio
   escreva("Insira o valor de x: ")
   leia(x)
   escreva("Insira o valor de y: ")
   leia(y)
   
   se (((x^2) - (y^2)) = 0) entao
      escreval("f(x) é indefinido (divisão por 0).")
   senao
      fx <- (2 * x * (y^2) - 10) / ((x^2) - (y^2))
      escreval("O valor de f(", x, ", ", y, ") é ", fx, ".")
   fimse
Fimalgoritmo
