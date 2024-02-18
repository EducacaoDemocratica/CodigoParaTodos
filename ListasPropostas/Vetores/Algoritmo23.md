# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown
Algoritmo "Q23 - Vetor"
Var
  i, j, lsup, aux, achou, c: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º valor do vetor: ")
    leia(v[i])
    enquanto (v[i] <= 0) faca
      escreva("Insira valores maiores que 0: ")
      leia(v[i])
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

  i <- 1

  enquanto (i < lsup) faca
    achou <- 0

    se (i = (lsup - 1)) entao
      se (v[i] = v[i + 1]) entao
        achou <- 1
      fimse
    senao
      enquanto (v[i] = v[i + 1]) faca
        achou <- 1
        i <- i + 1
      fimenquanto
    fimse

    se (achou = 1) entao
      c <- c + 1
    fimse

    i <- i + 1
  fimenquanto

  escreva("Pós ordenação: ")

  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  escreval(c, " números se repetem.")

Fimalgoritmo
