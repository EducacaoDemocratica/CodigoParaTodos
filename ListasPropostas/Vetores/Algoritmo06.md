# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - Vetor"
Var
  i, lsup: inteiro
  v: vetor [1..10] de inteiro
  d: vetor [1..10] de real
  va, dp, m: real

Inicio
  lsup <- 10
  m <- 0
  va <- 0

  para i de 1 ate lsup faca
    escreva("Insira o ", i, "º número do vetor: ")
    leia(v[i])
  fimpara

  escreval

  para i de 1 ate lsup faca
    m <- m + v[i]
  fimpara

  m <- m/i

  para i de 1 ate lsup faca
    d[i] <- v[i] - m
  fimpara

  para i de 1 ate lsup faca
    va <- va + (d[i] ^ 2)
  fimpara

  va <- va/i
  dp <- (va ^ (1/2))

  escreval("Média:", m)
  escreval("Variância:", va:6:2)
  escreval("Desvio padrão:", dp:6:2)

Fimalgoritmo
