# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown
Algoritmo "Q20 - Condicional"
Var
   s, a, b, c, d, den, num: real
Inicio
   escreva("Insira o valor de a: ")
   leia(a)
   escreva("Insira o valor de b: ")
   leia(b)
   escreva("Insira o valor de c: ")
   leia(c)
   escreva("Insira o valor de d: ")
   leia(d)
   
   den <- a * b * c * d

   se (den = 0) entao
      escreval("O somatório é indefinido (divisão por 0).")
   senao
      num <- ((a^2) + (b^2) + (c^2) + (d^2)) ^ (1/2)
      s <- num / den
      escreval("O valor do somatório é ", s, ".")
   fimse
Fimalgoritmo
