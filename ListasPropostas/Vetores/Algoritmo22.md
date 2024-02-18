# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown
Algoritmo "Q22 - Vetor"
Var
  i, j, lsup, aux, maior, c: inteiro
  v: vetor [1..30] de inteiro

Inicio
  lsup <- 30

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º valor do vetor: ")
    leia(v[i])
    enquanto (v[i] <= 0) faca
      escreva("Insira valores maiores que 0: ")
      leia(v[i])
    fimenquanto
  fimpara

  escreval

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (v[i] > v[i + 1]) entao
        aux <- v[i]
        v[i] <- v[i + 1]
        v[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval("Pós ordenação: ")

  para i de 1 ate lsup faca
    se ((i-1) mod 10 = 0) entao
      escreval
    fimse
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  maior <- 0
  c <- 0

  para i de 1 ate (lsup - 1) faca
    se ((v[i] + 1) = v[i + 1]) entao
      c <- c + 1
    senao
      c <- 0
    fimse
    se (c > maior) entao
      maior <- c
    fimse
  fimpara

  se (maior <> 0) entao
    maior <- maior + 1
  fimse

  escreval
  escreval("A sequência consecutiva possui", maior, " números.")

Fimalgoritmo
