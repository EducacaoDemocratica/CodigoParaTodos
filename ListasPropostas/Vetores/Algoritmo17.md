# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown
Algoritmo "Q17 - Vetor"
Var
  i, j, f, lsup: inteiro
  v: vetor [1..50] de real
  aux: real
  ordem: caractere

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º número do vetor: ")
    leia(v[i])
  fimpara

  escreval
  escreval("Escolhe uma função: ")
  escreval("0 - ordenar em ordem crescente")
  escreval("1 - ordenar em ordem decrescente")
  escreval
  escreva("Selecione um número: ")
  leia(f)

  enquanto ((f < 0) ou (f > 1)) faca
    escreva("Função inválida. Insira 0 ou 1: ")
    leia(f)
  fimenquanto

  escreval
  escreva("Vetor antes da ordenação:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i]:6:2, ".")
    senao
      escreva(v[i]:6:2, ",")
    fimse
  fimpara

  se (f = 0) entao
    ordem <- "crescente"

    para j de (lsup - 1) ate 1 passo -1 faca
      para i de 1 ate j faca
        se (v[i] > v[i + 1]) entao
          aux <- v[i]
          v[i] <- v[i + 1]
          v[i + 1] <- aux
        fimse
      fimpara
    fimpara

  senao
    ordem <- "decrescente"

    para j de (lsup - 1) ate 1 passo -1 faca
      para i de 1 ate j faca
        se (v[i] < v[i + 1]) entao
          aux <- v[i]
          v[i] <- v[i + 1]
          v[i + 1] <- aux
        fimse
      fimpara
    fimpara
  fimse

  escreval
  escreva("Vetor após a ordenação em ordem ", ordem, ":")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i]:6:2, ".")
    senao
      escreva(v[i]:6:2, ",")
    fimse
  fimpara

Fimalgoritmo
