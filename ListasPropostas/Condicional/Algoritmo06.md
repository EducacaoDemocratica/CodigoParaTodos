# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - Condicional"
Var
   n1, n2, n3, n4, n5, n6, r1, r2, r3, r4, r5: real
   r: logico
Inicio
   r <- falso
   r1 <- 999
   r2 <- 999
   r3 <- 999
   r4 <- 999
   r5 <- 999

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
      escreva("Números repetidos:")

      se ((n1 = n2) ou (n1 = n3) ou (n1 = n4) ou (n1 = n5) ou (n1 = n6)) entao
         r1 <- n1
      fimse

      se ((n2 = n3) ou (n2 = n4) ou (n2 = n5) ou (n2 = n6)) entao
         r2 <- n2
      fimse

      se ((n3 = n4) ou (n3 = n5) ou (n3 = n6)) entao
         r3 <- n3
      fimse

      se ((n4 = n5) ou (n4 = n6)) entao
         r4 <- n4
      fimse

      se ((n5 = n6)) entao
         r5 <- n5
      fimse

      se (r1 <> 999) entao
         escreva(r1, " ")
      fimse

      se ((r2 <> 999) e (r2 <> r1) e (r2 <> r3) e (r2 <> r4) e (r2 <> r3)) entao
         escreva(r2, " ")
      fimse

      se ((r3 <> 999) e (r3 <> r1) e (r3 <> r4) e (r3 <> r5)) entao
         escreva(r3, " ")
      fimse

      se ((r4 <> 999) e (r4 <> r1) e (r4 <> r5)) entao
         escreva(r4, " ")
      fimse

      se ((r5 <> 999) e (r5 <> r1)) entao
         escreva(r5, " ")
      fimse

   senao
      escreval("Não existem números iguais.")
   fimse
Fimalgoritmo
