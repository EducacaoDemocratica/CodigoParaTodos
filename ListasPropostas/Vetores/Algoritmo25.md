# Exercício 25

[**Ver Análise**](Analise25.md)

```markdown
Algoritmo "Q25 - Vetor"
Var
  i, j, k, lsup, aux, achou: inteiro
  v, vaux: vetor [1..20] de inteiro

Inicio
  lsup <- 20

  para i de 1 ate lsup faca
    escreva("Insira o",i,"º valor do vetor: ")
    leia (v[i])
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (v[i] > v[i + 1]) entao
        aux <- v[i]
        v[i] <- v[i + 1]
        v[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval

  escreva("Vetor original: ")

  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  k <- 0

  para i de 1 ate lsup faca
    achou <- 1

    para j de 1 ate lsup faca
      se (vaux[j] = v[i]) entao
        achou <- 0
      fimse
    fimpara

    se (achou = 1) entao
      k <- k + 1
      vaux[k] <- v[i]
    fimse
  fimpara

  para j de (k - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (v[i] > v[i + 1]) entao
        aux <- v[i]
        v[i] <- v[i + 1]
        v[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreva("Vetor sem repetições: ")

  para i de 1 ate k faca
    se (i = lsup) entao
      escreval(vaux[i], ".")
    senao
      escreva(vaux[i], ",")
    fimse
  fimpara

Fimalgoritmo
