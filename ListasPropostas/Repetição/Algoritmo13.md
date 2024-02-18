# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown
Algoritmo "Q13 - Repeticao"
Var
   n, aux, s: inteiro
Inicio
   s <- 0
   aux <- 0
   escreva("Insira um número inteiro positivo: ")
   leia(n)
   
   enquanto (n <= 0) faca
      escreva("O número deve ser maior que zero: ")
      leia(n)
   fimenquanto
   
   escreval
   
   enquanto (aux < n) faca
      aux <- aux + 1
      se ((n mod aux = 0) e (aux <> n)) entao
         s <- s + aux
      fimse
   fimenquanto
   
   se (s = n) entao
      escreval("O número", n," é perfeito.")
   senao
      escreval("O número", n," não é perfeito.")
   fimse
Fimalgoritmo
