# Exercício 21

[**Ver Análise**](Analise21.md)

```markdown
Algoritmo "Q21 - Repeticao"
Var
   n, aux, s, t, i: inteiro
Inicio
   escreva("Insira um número inteiro positivo: ")
   leia(n)
   
   enquanto (n <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(n)
   fimenquanto
   
   escreval
   
   aux <- 0
   s <- 0
   
   enquanto (aux < n) faca
      aux <- aux + 1
      se ((n mod aux = 0) e (aux <> n)) entao
         s <- s + aux
      fimse
   fimenquanto
   
   se (s = n) entao
      escreval(" O número", n," é perfeito.")
      escreval(n, " também é triângular pois é o somatório de: ")
      escreval
   
      i <- 0
      t <- 0
      
      enquanto (t <> s) faca
         i <- i + 1
         t <- t + i
         
         se (i mod 10 = 0) entao
            escreval
         fimse
         
         se (t = s) entao
            escreval(i,"")
         senao
            escreva(i," +")
         fimse
      fimenquanto
      
   senao
      escreval("O número",n," não é perfeito!")
   fimse
Fimalgoritmo
