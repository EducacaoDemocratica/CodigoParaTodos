# Exercício 44

[**Ver Análise**](Analise44.md)

```markdown
Algoritmo "Q44 - Vetor"
Var
  i, j, lsup, aux: inteiro
  a: vetor [1..10] de inteiro

Inicio
  lsup <- 6
  escreva("Insira a quantidade de números da sua aposta: ")
  leia(lsup)

  enquanto ((lsup < 6) ou (lsup > 10)) faca
    escreva("Insira de 6 a 10 números em sua aposta: ")
    leia(lsup)
  fimenquanto

  para i de 1 ate lsup faca
    escreva("Insira o ", i,"º número da aposta: ")
    leia(a[i])

    enquanto ((a[i] <= 0) ou (a[i] > 60)) faca
      escreva("Insira valores de 1 a 60: ")
      leia(a[i])
    fimenquanto

    j <- 1
    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (a[i] = a[j]) faca
          escreva("Esse valor já está na aposta: ")
          leia (a[i])

          enquanto ((a[i] <= 0) ou (a[i] > 60)) faca
            escreva("Insira valores de 1 a 60: ")
            leia(a[i])
          fimenquanto
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (a[i] > a[i + 1]) entao
        aux <- a[i]
        a[i] <- a[i + 1]
        a[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval
  escreva("Números da aposta: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(a[i], ".")
    senao
      escreva(a[i], ",")
    fimse
  fimpara
Fimalgoritmo
