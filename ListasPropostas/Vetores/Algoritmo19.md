# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - Vetor"
Var
  i, j, lsup, aux, p: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º valor do vetor: ")
    leia (v[i])
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (v[i] < v[i + 1]) entao
        aux <- v[i]
        v[i] <- v[i + 1]
        v[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval
  p <- 5
  escreval("O", p, "º maior número inserido é", v[p], ".")

Fimalgoritmo
