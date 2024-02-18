# Exercício Q1 

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - Vetor"
Var
  i, lsup, q: inteiro
  n: vetor [1..35] de real
  m: real

Inicio
  lsup <- 35
  m <- 0
  q <- 0

  para i de 1 ate lsup faca
    escreva("Insira a nota do ", i, "º candidato: ")
    leia(n[i])

    enquanto ((n[i] < 0) ou (n[i] > 10)) faca
      escreva("A nota deve estar entre 0 e 10: ")
      leia(n[i])
    fimenquanto

  fimpara

  para i de 1 ate lsup faca
    m <- m + n[i]
  fimpara

  m <- m/i

  para i de 1 ate lsup faca
    se (n[i] > m) entao
      q <- q + 1
    fimse
  fimpara

  escreval
  escreval("A média das notas inseridas é ", m:6:2,".")
  escreval(q, " candidatos ficaram com notas acima da média.")
Fimalgoritmo
