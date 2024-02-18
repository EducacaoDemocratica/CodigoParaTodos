# Exercício 24

[**Ver Análise**](Analise24.md)

```markdown
Algoritmo "Q24 - Vetor"
Var
  i, j, k, lsup, aux, achou: inteiro
  v, vaux, r: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º valor do vetor: ")
    leia (v[i])
    enquanto ((v[i] < 3) ou (v[i] > 8)) faca
      escreva("Insira inteiros do intervalo [3, 8]:")
      leia (v[i])
    fimenquanto
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

  escreva("Pós ordenação: ")

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
        r[j] <- r[j] + 1
        achou <- 0
      fimse
    fimpara

    se (achou = 1) entao
      k <- k + 1
      vaux[k] <- v[i]
      r[k] <- 0
    fimse
  fimpara

  para i de 1 ate k faca
    escreval(vaux[i], " repete", r[i], " vezes.")
  fimpara

Fimalgoritmo
