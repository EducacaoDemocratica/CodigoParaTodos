# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown
Algoritmo "Q13 - Condicional"
Var
   n, n2, aux1, aux2, aux3, aux4, r1, r2, r3: inteiro
   t: logico
Inicio
   t <- falso
   r1 <- 999
   r2 <- 999
   r3 <- 999
   escreva("Insira um número de 4 dígitos: ")
   leia(n)
   escreval

   se ((n div 1000 = 0) ou (n div 1000 >= 10)) entao
      escreval("Erro: o número inserido não possui 4 dígitos.")
   senao
      n2 <- n
      aux1 <- n2 div 1000
      n2 <- n2 - (aux1 * 1000)
      aux2 <- n2 div 100
      n2 <- n2 - (aux2 * 100)
      
      se (aux1 = aux2) entao
         t <- verdadeiro
         r1 <- aux2
      fimse

      aux3 <- n2 div 10
      n2 <- n2 - (aux3 * 10)
      
      se ((aux1 = aux3) ou (aux2 = aux3)) entao
         t <- verdadeiro
         r2 <- aux3
      fimse

      aux4 <- n2
      
      se ((aux1 = aux4) ou (aux2 = aux4) ou (aux3 = aux4)) entao
         t <- verdadeiro
         r3 <- aux4
      fimse

      se (t = falso) entao
         escreval("Não há algarismos repetidos no número", n,".")
      senao
         escreva("Números repetidos: ")
         
         se (r1 <> 999) entao
            escreva(r1, " ")
         fimse

         se ((r2 <> 999) e (r2 <> r1)) entao
            escreva(r2, " ")
         fimse

         se ((r3 <> 999) e (r3 <> r1) e (r3 <> r2)) entao
            escreva(r3, " ")
         fimse
      fimse
   fimse
Fimalgoritmo
