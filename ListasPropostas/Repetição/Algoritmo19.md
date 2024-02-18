# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - Repeticao"
Var
   linf, lsup, i, s, aux: inteiro
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
   
   se (linf > lsup) entao
      escreval
      escreval("Corrigindo os valores.")
      aux <- lsup
      lsup <- linf
      linf <- aux
   fimse
   
   escreval
   i <- linf
   s <- linf
   
   enquanto (i < lsup) faca
      i <- i + 1
      s <- s + i
   fimenquanto
   
   escreval("O somatório dos valores do intervalo [", linf,",", lsup,"] é", s,".")
Fimalgoritmo
