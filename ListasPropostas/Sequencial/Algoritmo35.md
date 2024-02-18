# Exercício 35

[**Ver Análise**](Analise35.md)

```markdown
Algoritmo "Q35 - Sequencial"
Var
   htotal, h1, h2, h3, p1, p2, p3: real
   i1, i2, i3, s: inteiro
Inicio
   escreva("Insira o valor total da herança: R$")
   leia(htotal)
   escreva("Insira a idade do primeiro irmão: ")
   leia(i1)
   escreva("Insira a idade do segundo irmão: ")
   leia(i2)
   escreva("Insira a idade do terceiro irmão: ")
   leia(i3)
   escreval
   s <- i1 + i2 + i3
   p1 <- (i1/s)
   p2 <- (i2/s)
   p3 <- (i3/s)
   h1 <- htotal * p1
   h2 <- htotal * p2
   h3 <- htotal * p3
   p1 <- p1 * 100
   p2 <- p2 * 100
   p3 <- p3 * 100
   escreval("Herança total: R$", htotal:6:2, ".")
   escreval("Parte do primeiro irmão: R$", h1:6:2, "=", p1:6:2, "%.")
   escreval("Parte do segundo irmão: R$", h2:6:2, "=", p2:6:2, "%.")
   escreval("Parte do terceiro irmão: R$", h3:6:2, "=", p3:6:2, "%.")
Fimalgoritmo
