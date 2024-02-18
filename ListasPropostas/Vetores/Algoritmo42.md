# Exercício 42

[**Ver Análise**](Analise42.md)

```markdown
Algoritmo "Q42 - Vetor"
Var
  i, j, k, lsupa, lsupb, aux, achou: inteiro
  a: vetor [1..30] de inteiro
  b, c: vetor [1..20] de inteiro

Inicio
  escreva("Insira um número: ")
  leia(lsupa)

  enquanto ((lsupa <= 0) ou (lsupa > 30)) faca
    escreva("Insira um número maior que 0 e menor/igual a 30: ")
    leia(lsupa)
  fimenquanto

  escreval

  para i de 1 ate lsupa faca
    escreva("Insira o", i, "º valor do vetor A: ")
    leia(a[i])
    j <- 1
    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (a[i] = a[j]) faca
          escreva("Esse valor já está no vetor A: ")
          leia(a[i])
          j <- 1
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  para j de (lsupa - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (a[i] > a[i + 1]) entao
        aux <- a[i]
        a[i] <- a[i + 1]
        a[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval

  escreva("Insira um número: ")
  leia(lsupb)

  enquanto ((lsupb <= 0) ou (lsupb > 20)) faca
    escreva("Insira um número maior que 0 e menor/igual a 20: ")
    leia(lsupb)
  fimenquanto

  escreval

  para i de 1 ate lsupb faca
    escreva("Insira o", i, "º valor do vetor B: ")
    leia(b[i])
    j <- 1
    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (b[i] = b[j]) faca
          escreva("Esse valor já está no vetor B: ")
          leia(b[i])
          j <- 1
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  para j de (lsupb - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (b[i] > b[i + 1]) entao
        aux <- b[i]
        b[i] <- b[i + 1]
        b[i + 1] <- aux
      fimse
    fimpara
  fimpara

  k <- 0

  para i de 1 ate lsupa faca
    achou <- 1
    para j de 1 ate k faca
      se (c[j] = a[i]) entao
        achou <- 0
      fimse
    fimpara
    se (achou = 1) entao
      k <- k + 1
      c[k] <- a[i]
    fimse
  fimpara

  para i de 1 ate lsupb faca
    achou <- 1
    para j de 1 ate k faca
      se (c[j] = b[i]) entao
        achou <- 0
      fimse
    fimpara
    se (achou = 1) entao
      k <- k + 1
      c[k] <- b[i]
    fimse
  fimpara

  para j de (k - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (c[i] > c[i + 1]) entao
        aux <- c[i]
        c[i] <- c[i + 1]
        c[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval

  escreva("A: ")
  para i de 1 ate lsupa faca
    se (i = lsupa) entao
      escreval(a[i], ".")
    senao
      escreva(a[i], ",")
    fimse
  fimpara

  escreva("B: ")
  para i de 1 ate lsupb faca
    se (i = lsupb) entao
      escreval(b[i], ".")
    senao
      escreva(b[i], ",")
    fimse
  fimpara

  escreva("C: ")
  para i de 1 ate k faca
    se (i = k) entao
      escreval(c[i], ".")
    senao
      escreva(c[i], ",")
    fimse
  fimpara

Fimalgoritmo
