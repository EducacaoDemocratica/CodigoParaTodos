# Exercício 38

[**Ver Análise**](Analise38.md)

```markdown
 Algoritmo "Q38 - Vetor"

Var
  i, j, k, p, lsupa, lsupb, aux, achou: inteiro
  a: vetor [1..7] de inteiro
  b: vetor [1..9] de inteiro
  c: vetor [1..7] de inteiro

Inicio
  lsupa <- 7
  lsupb <- 9

  para i de 1 ate lsupa faca
    escreva("Insira o",i,"º elemento de A: ")
    leia(a[i])
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
    leia(b[i])
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
    para p de 1 ate lsupb faca
      achou <- 0
      se (a[i] = b[p]) entao
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
      fimse
    fimpara
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
