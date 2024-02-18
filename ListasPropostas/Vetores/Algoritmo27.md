# Exercício 27

[**Ver Análise**](Analise27.md)

```markdown
Algoritmo "Q27 - Vetor"
Var
  i, lsup, j, aux, p: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º valor do vetor: ")
    leia (v[i])

    enquanto (v[i] = 0) faca
      escreva("Não insira o número 0: ")
      leia (v[i])
    fimenquanto

    j <- 1

    enquanto (j < lsup) faca
      se (j <> i) entao
        enquanto (v[i] = v[j]) faca
          escreva("Esse valor já está no vetor: ")
          leia (v[i])

          enquanto (v[i] = 0) faca
            escreva("Não insira o número 0: ")
            leia (v[i])
          fimenquanto
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
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
  p <- 3
  escreval("O", p, "º maior número inserido é", v[p], ".")

Fimalgoritmo
