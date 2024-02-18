# Exercício 39

[**Ver Análise**](Analise39.md)

```markdown
Algoritmo "Q39 - Repeticao"
Var
   linf, lsup, s, n, no, aux, aux2, c, a, sa, k: inteiro
Inicio
   escreva("Insira o limite inferior do intervalo: ")
   leia(linf)
   escreva("Insira o limite superior do intervalo: ")
   leia(lsup)

   se (lsup < linf) entao
      aux <- linf
      linf <- lsup
      lsup <- aux
   fimse

   escreva("Insira o valor da soma dos algarismos (S): ")
   leia(s)

   enquanto (s < 0) faca
      escreva("O valor da soma não pode ser negativo: ")
      leia(s)
   fimenquanto

   escreval
   escreval("Números do intervalo [", linf, ",", lsup, "] cuja soma dos algarismos é", s, ": ")

   para n de linf ate lsup faca
      sa <- 0
      no <- n
      c <- -1
      aux <- 1
      aux2 <- 1

      enquanto (c <> 0) faca
         c <- n div aux
         aux <- aux * 10
      fimenquanto

      aux <- aux div 100
      aux2 <- 1

      enquanto (aux > 0) faca
         a <- n div aux
         n <- n - a * aux
         aux <- aux div 10
         sa <- sa + a
      fimenquanto

      se (sa = s) entao
         k <- k + 1
         se (k = 1) entao
            escreva(no)
         senao
            escreva(",", no)
         fimse
      fimse

      se (no = lsup) entao
         escreval(".")
      fimse
   fimpara
Fimalgoritmo
