# Exercício 40

[**Ver Análise**](Analise40.md)

```markdown
Algoritmo "Q40 - Vetor"
Var
  i, j, k, p, lsupa, lsupb, aux, achou: inteiro
  a: vetor [1..8] de inteiro
  b, c: vetor [1..5] de inteiro

Inicio
  lsupa <- 8
  lsupb <- 5

  para i de 1 ate lsupa faca
    escreva("Insira o",i,"º elemento de A: ")
    leia (a[i])
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

  para i de 1 ate lsupb faca
    escreva("Insira o",i,"º elemento de B: ")
    leia (b[i])
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
  para i de 1 ate lsupb faca
    achou <- 1
    para p de 1 ate lsupb faca
      se (a[p] <= b[i]) entao
        se (b[i] = a[p]) entao
          achou <- 0
        fimse
      fimse
    fimpara

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
