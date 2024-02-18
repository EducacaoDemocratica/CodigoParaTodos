# Exercício 50 - Sequencial

[**Ver Análise**](Analise50.md)

```markdown
Algoritmo "Q50 - Sequencial"
Var
   i, n, no, um, cinco, dez, cinquenta, cem, quinhentos: inteiro
Inicio
   um <- 0
   cinco <- 0
   dez <- 0
   cinquenta <- 0
   cem <- 0
   quinhentos <- 0

   escreva("Insira um número inteiro: ")
   leia(n)

   enquanto ((n <= 0) ou (n >= 1000)) faca
      escreva("O número deve estar entre 1 a 999: ")
      leia(n)
   fimenquanto

   no <- n
   quinhentos <- n div 500
   n <- n - quinhentos * 500
   cem <- n div 100
   n <- n - cem * 100
   cinquenta <- n div 50
   n <- n - cinquenta * 50
   dez <- n div 10
   n <- n - dez * 10
   cinco <- n div 5
   n <- n - cinco * 5
   um <- n

   escreva("A representação romana de", no," é: ")

   se ((quinhentos + cem) = 5) entao
      escreva("CM")
   senao
      se (cem = 4) entao
         escreva("CD")
      senao
         para i de 1 ate quinhentos faca
            escreva("D")
         fimpara

         para i de 1 ate cem faca
            escreva("C")
         fimpara
      fimse
   fimse

   se ((cinquenta + dez) = 5) entao
      escreva("XC")
   senao
      se (dez = 4) entao
         escreva("XL")
      senao
         para i de 1 ate cinquenta faca
            escreva("L")
         fimpara

         para i de 1 ate dez faca
            escreva("X")
         fimpara
      fimse
   fimse

   se ((cinco + um) = 5) entao
      escreva("IX")
   senao
      se (um = 4) entao
         escreva("IV")
      senao
         para i de 1 ate cinco faca
            escreva("V")
         fimpara

         para i de 1 ate um faca
            escreva("I")
         fimpara
      fimse
   fimse
Fimalgoritmo
