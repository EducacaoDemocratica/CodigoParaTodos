# Exercício 41

[**Ver Análise**](Analise41.md)

```markdown
Algoritmo "Q41 - Vetor"
Var
  i, j, k, p, lsupa, lsupb, aux: inteiro
  a, aaux, b, baux: vetor [1..6] de inteiro
  contido: logico

Inicio
  contido <- verdadeiro
  lsupa <- 6
  lsupb <- 13
  k <- 0
  p <- 0

  para i de 1 ate lsupa faca
    escreva("Insira o", i, "º elemento de A: ")
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

  para i de 1 ate lsupa faca
    achou <- 1
    para j de 1 ate lsupa faca
      se (aaux[j] = a[i]) entao
        achou <- 0
      fimse
    fimpara
    se (achou = 1) entao
      k <- k + 1
      aaux[k] <- a[i]
    fimse
  fimpara

  escreval

  para i de 1 ate lsupb faca
    escreva("Insira o", i, "º elemento de B: ")
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

  para i de 1 ate lsupb faca
    achou <- 1
    para j de 1 ate lsupb faca
      se (baux[j] = b[i]) entao
        achou <- 0
      fimse
    fimpara
    se (achou = 1) entao
      p <- p + 1
      baux[p] <- b[i]
    fimse
  fimpara

  i <- 1
  enquanto ((i <= k) e (contido = verdadeiro)) faca
    contido <- falso
    para j de 1 ate p faca
      se (aaux[i] = baux[j]) entao
        contido <- verdadeiro
      fimse
    fimpara
    i <- i + 1
  fimenquanto

  escreval

  se (contido = verdadeiro) entao
    escreval("A está contido em B.")
  senao
    escreval("A não está contido em B.")
  fimse

Fimalgoritmo
