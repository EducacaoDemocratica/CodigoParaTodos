# Exercício 24

[**Ver Análise**](Analise24.md)

```markdown
Algoritmo "Q24 - Condicional"
Var
   p1, p2, p3, s, vp, menor: real
Inicio
   s <- 0
   escreva("Insira o preço do produto 1: ")
   leia(p1)

   se (p1 <= 0) entao
      escreval("Erro: não há preço negativo ou nulo.")
   senao
      menor <- p1
      escreva("Insira o preço do produto 2: ")
      leia(p2)

      se (p2 <= 0) entao
         escreval("Erro: não há preço negativo ou nulo.")
      senao
         se (p2 < menor) entao
            menor <- p2
         fimse

         escreva("Insira o preço do produto 3: ")
         leia(p3)

         se (p3 <= 0) entao
            escreval("Erro: não há preço negativo ou nulo.")
         senao
            se (p3 < menor) entao
               menor <- p3
            fimse

            s <- s + p1 + p2 + p3
            vp <- s - menor
            escreval("Valor dos três produtos: R$", s)
            escreval("Valor pago: R$", vp)
         fimse
      fimse
   fimse
Fimalgoritmo
