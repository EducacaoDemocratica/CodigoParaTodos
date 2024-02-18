# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - Condicional"
Var
   n1, n2, n3, n4, n5, n6: real
   r: logico
Inicio
   r <- falso
   escreva("Insira um número: ")
   leia(n1)
   escreva("Insira um número: ")
   leia(n2)
   se (n1 = n2) entao
      r <- verdadeiro
   fimse
   escreva("Insira um número: ")
   leia(n3)
   se ((n1 = n3) ou (n2 = n3)) entao
      r <- verdadeiro
   fimse
   escreva("Insira um número: ")
   leia(n4)
   se ((n1 = n4) ou (n2 = n4) ou (n3 = n4)) entao
      r <- verdadeiro
   fimse
   escreva("Insira um número: ")
   leia(n5)
   se ((n1 = n5) ou (n2 = n5) ou (n3 = n5) ou (n4 = n5)) entao
      r <- verdadeiro
   fimse
   escreva("Insira um número: ")
   leia(n6)
   se ((n1 = n6) ou (n2 = n6) ou (n3 = n6) ou (n4 = n6) ou (n5 = n6)) entao
      r <- verdadeiro
   fimse
   escreval
   se (r = verdadeiro) entao
      escreval("Existem números que se repetem.")
   senao
      escreval("Não existem números que se repetem.")
   fimse
Fimalgoritmo
# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - Condicional"
Var
   n1, n2, n3, n4, n5, menor: real
Inicio
   escreva("Insira um número: ")
   leia(n1)
   menor <- n1
   escreva("Insira um número: ")
   leia(n2)
   se (n2 < menor) entao
      menor <- n2
   fimse
   escreva("Insira um número: ")
   leia(n3)
   se (n3 < menor) entao
      menor <- n3
   fimse
   escreva("Insira um número: ")
   leia(n4)
   se (n4 < menor) entao
      menor <- n4
   fimse
   escreva("Insira um número: ")
   leia(n5)
   se (n5 < menor) entao
      menor <- n5
   fimse
   escreval
   se ((n1 = n2) e (n2 = n3) e (n3 = n4) e (n4 = n5)) entao
      escreval("Não há um menor número porque todos são iguais.")
   senao
      escreval("O menor número é", menor,".")
   fimse
Fimalgoritmo
