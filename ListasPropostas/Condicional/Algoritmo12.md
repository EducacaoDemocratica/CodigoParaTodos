# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown
Algoritmo "Q12 - Condicional"
Var
   n, n2, aux1, aux2, aux3, aux4, maior: inteiro
Inicio
   escreva("Insira um número de 4 dígitos: ")
   leia(n)
   escreval

   se ((n div 1000 = 0) ou (n div 1000 >= 10)) entao
      escreval("Erro: o número inserido não possui 4 dígitos.")
   senao
      se (n < 0) entao
         n <- -n
      fimse

      n2 <- n
      aux1 <- n2 div 1000
      maior <- aux1
      n2 <- n2 - (aux1 * 1000)
      aux2 <- n2 div 100
      n2 <- n2 - (aux2 * 100)
      
      se (aux2 > maior) entao
         maior <- aux2
      fimse

      aux3 <- n2 div 10
      n2 <- n2 - (aux3 * 10)
      
      se (aux3 > maior) entao
         maior <- aux3
      fimse

      aux4 <- n2
      
      se (aux4 > maior) entao
         maior <- aux4
      fimse

      escreval("O algarismo de maior valor absoluto do número", n, " é", maior,".")
   fimse
Fimalgoritmo
