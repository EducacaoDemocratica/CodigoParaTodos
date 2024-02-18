# Exercício 47 - Repetição

[**Ver Análise**](Analise47.md)

```markdown
Algoritmo "Q47 - Repeticao"
Var
   i, n, den: inteiro
   s: real
Inicio
   escreva("Insira o valor de n: ")
   leia(n)
   
   enquanto (n <= 0) faca
      escreva("n deve ser maior que zero: ")
      leia(n)
   fimenquanto
   
   escreval
   den <- n
   para i de 1 ate n faca
      s <- s + i/den
      den <- den - 1
   fimpara

   escreval("O valor de s com", n, " números é", s)
Fimalgoritmo
