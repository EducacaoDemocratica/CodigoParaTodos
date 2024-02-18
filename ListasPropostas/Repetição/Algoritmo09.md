# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown
Algoritmo "Q9 - Repeticao"
Var
   x, y, maior, menor, aux: inteiro
Inicio
   escreva("Insira um número positivo x: ")
   leia(x)
   enquanto (x <= 0) faca
      escreva("O número deve ser positivo.")
      leia(x)
   fimenquanto
   escreva("Insira um número positivo y: ")
   leia(y)
   enquanto (y <= 0) faca
      escreva("O número deve ser positivo.")
      leia(y)
   fimenquanto
   escreval
   se(x > y) entao
      maior <- x
      menor <- y
   senao
      maior <- y
      menor <- x
   fimse
   enquanto (maior mod menor > 0) faca
      aux <- menor
      menor <- maior mod menor
      maior <- aux
   fimenquanto
   se(menor = 1) entao
      escreval("Os números são primos entre si.")
   senao
      escreval("Os números não são primos entre si.")
   fimse
Fimalgoritmo
