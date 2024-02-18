# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown
Algoritmo "Q11 - Condicional"
Var
   n, n2, aux1, aux2, aux3: inteiro
Inicio
   escreva("Insira um número de 4 dígitos: ")
   leia(n)
   escreval

   se (n < 0) entao
      escreval("Erro: número negativo inserido.")
   senao
      se ((n div 1000 = 0) ou (n div 1000 >= 10)) entao
         escreval("Erro: o número inserido não possui 4 dígitos.")
      senao
         n2 <- n
         aux1 <- n2 div 1000
         n2 <- n2 - (aux1 * 1000)
         aux2 <- n2 div 100
         n2 <- n2 - (aux2 * 100)
         aux3 <- n2 div 10
         n2 <- (n2 * 1000) + (aux3 * 100) + (aux2 * 10) + aux1

         se (n = n2) entao
            escreval("O número é capicua.")
         senao
            escreval("O número não é capicua.")
         fimse
      fimse
   fimse
Fimalgoritmo
