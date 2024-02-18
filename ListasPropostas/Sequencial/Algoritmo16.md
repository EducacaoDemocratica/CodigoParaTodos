# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown
Algoritmo "Q16 - Sequencial"
Var
   t, cem, cinq, vinte, dez, cinco, um, s: inteiro
Inicio
   s <- 0
   cem <- 0
   cinq <- 0
   vinte <- 0
   dez <- 0
   cinco <- 0
   um <- 0
   escreva("Insira o valor do troco: R$")
   leia(t)
   cem <- t div 100
   t <- t - cem * 100
   cinq <- t div 50
   t <- t - cinq * 50
   vinte <- t div 20
   t <- t - vinte * 20
   dez <- t div 10
   t <- t - dez * 10
   cinco <- t div 5
   t <- t - cinco * 5
   um <- t
   s <- cem + cinq + vinte + dez + cinco + um
   escreval("A quantidade mínima de cédulas de troco são", s, ", sendo elas: ")
   escreval
   escreval(cem, " cédulas de R$100,00.")
   escreval(cinq, " cédulas de R$50,00.")
   escreval(vinte, " cédulas de R$20,00.")
   escreval(dez, " cédulas de R$10,00.")
   escreval(cinco, " cédulas de R$5,00.")
   escreval(um, " cédulas de R$1,00.")
Fimalgoritmo
