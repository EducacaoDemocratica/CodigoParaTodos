# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown
Algoritmo "Q22 - Repeticao"
Var
   linf, lsup, i, p, aux: inteiro
Inicio
   escreva("Insira o limite inferior do conjunto: ")
   leia(linf)
   
   enquanto (linf < 0) faca
      escreva("Esse número não pode ser negativo: ")
      leia(linf)
   fimenquanto
   
   escreva("Insira o limite superior do conjunto: ")
   leia(lsup)
   
   enquanto (lsup < 0) faca
      escreva("Esse número não pode ser negativo: ")
      leia(lsup)
   fimenquanto
   
   escreval
   
   se (linf > lsup) entao
      escreval("Corrigindo os valores...")
      escreval
      aux <- lsup
      lsup <- linf
      linf <- aux
   fimse
   
   i <- linf
   p <- linf
   
   enquanto (i < lsup) faca
      i <- i + 1
      p <- p * i
   fimenquanto
   
   escreval("O produtório dos valores do intervalo [", linf,",", lsup,
"] é", p,".")
Fimalgoritmo
