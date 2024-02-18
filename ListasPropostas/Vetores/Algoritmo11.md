# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown
Algoritmo "Q11 - Vetor"
Var
  i, lsup, maiorp, menori, ni, np, j, k: inteiro
  v, par, imp: vetor [1..50] de inteiro
  mp, mi: real

Inicio
  lsup <- 10
  ni <- 0
  np <- 0
  mi <- 0
  mp <- 0
  j <- 0
  k <- 0

  para i de 1 ate lsup faca
    escreva("Insira o", i,"º número do vetor: ")
    leia(v[i])
  fimpara

  escreval

  para i de 1 ate lsup faca
    se (v[i] mod 2 = 0) entao
      np <- np + 1
      mp <- mp + v[i]

      se (np = 1) entao
        maiorp <- v[i]
      senao
        se (v[i] > maiorp) entao
          maiorp <- v[i]
        fimse
      fimse
    senao
      ni <- ni + 1
      mi <- mi + v[i]

      se (ni = 1) entao
        menori <- v[i]
      senao
        se (v[i] < menori) entao
          menori <- v[i]
        fimse
      fimse
    fimse
  fimpara

  mi <- mi/ni
  mp <- mp/np

  para i de 1 ate lsup faca
    se (v[i] mod 2 = 0) entao
      se (v[i] > mp) entao
        j <- j + 1
        par[j] <- v[i]
      fimse
    senao
      se (v[i] < mi) entao
        k <- k + 1
        imp[k] <- v[i]
      fimse
    fimse
  fimpara

  escreval("Média dos números pares:", mp:6:2)
  escreval("Média dos números ímpares:", mi:6:2)
  escreval("Maior par inserido: ", maiorp)
  escreval("Menor ímpar inserido: ", menori)
  escreva("Pares maiores que a média par: ")

  para i de 1 ate j faca
    se (i = j) entao
      escreval(par[i],".")
    senao
      escreva(par[i],",")
    fimse
  fimpara

  escreva("Ímpares menores que a média ímpar: ")

  para i de 1 ate k faca
    se (i = k) entao
      escreval(imp[i],".")
    senao
      escreva(imp[i],",")
    fimse
  fimpara

Fimalgoritmo
