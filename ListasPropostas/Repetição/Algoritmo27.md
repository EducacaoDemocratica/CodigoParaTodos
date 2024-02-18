# Exercício 27

[**Ver Análise**](Analise27.md)

```markdown
Algoritmo "Q27 - Repeticao"
Var
   n1, i, r, aux: inteiro
Inicio
   r <- 0
   i <- 0
   aux <- -1
   escreva("Insira um número positivo: ")
   leia(n1)
   
   enquanto (n1 < 0) faca
      escreva("O número deve ser positivo. Leia novamente: ")
      leia(n1)
   fimenquanto
   
   escreval
   escreva("Parte inteira da raiz quadrada de", n1,":")
   
   enquanto (r < n1) faca
      aux <- aux + 2
      r <- r + aux
      i <- i + 1
      se (r > n1) entao
         i <- i - 1
      fimse
   fimenquanto
   
   escreval(i)
Fimalgoritmo
