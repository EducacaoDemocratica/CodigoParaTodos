# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - Condicional"
Var
   n1, n2, n3, n4, n5, n6, s: inteiro
Inicio
   s <- 0
   escreval("Insira seis numeros!")
   escreval
   escreva("Insira o 1º número: ")
   leia(n1)
   se (n1 mod 2 = 0) entao
      s <- s + n1
   fimse
   escreva("Insira o 2º número: ")
   leia(n2)
   se (n2 mod 2 = 0) entao
      s <- s + n2
   fimse
   escreva("Insira o 3º número: ")
   leia(n3)
   se (n3 mod 2 = 0) entao
      s <- s + n3
   fimse
   escreva("Insira o 4º número: ")
   leia(n4)
   se (n4 mod 2 = 0) entao
      s <- s + n4
   fimse
   escreva("Insira o 5º número: ")
   leia(n5)
   se (n5 mod 2 = 0) entao
      s <- s + n5
   fimse
   escreva("Insira o 6º número: ")
   leia(n6)
   se (n6 mod 2 = 0) entao
      s <- s + n6
   fimse
   escreval
   escreval("A soma dos números pares é", s,".")
Fimalgoritmo
