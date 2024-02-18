# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown
Algoritmo "Q3 - Condicional"
Var
   n1, n2, n3, n4, maior: real
Inicio
   escreva("Insira um número: ")
   leia(n1)
   maior <- n1
   escreva("Insira um número: ")
   leia(n2)
   se (n2 > maior) entao
      maior <- n2
   fimse
   escreva("Insira um número: ")
   leia(n3)
   se (n3 > maior) entao
      maior <- n3
   fimse
   escreva("Insira um número: ")
   leia(n4)
   se (n4 > maior) entao
      maior <- n4
   fimse
   escreval
   se ((n1 = n2) e (n2 = n3) e (n3 = n4)) entao
      escreval("Não há um maior número porque todos são iguais.")
   senao
      escreval("O maior número é", maior,".")
   fimse
Fimalgoritmo
