# Exercício Q2 

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - Vetor"
Var
  i, lsup: inteiro
  n: vetor [1..15] de real
  m: real

Inicio
  lsup <- 10
  m <- 0

  para i de 1 ate lsup faca
    escreva("Insira a nota do ", i, "º candidato: ")
    leia(n[i])

    enquanto ((n[i] < 0) ou (n[i] > 100)) faca
      escreva("A nota deve estar entre 0 e 10: ")
      leia(n[i])
    fimenquanto

  fimpara

  para i de 1 ate lsup faca
    m <- m + n[i]
  fimpara

  m <- m/i

  escreval
  escreval("A média das notas inseridas é ", m:6:2,".")
Fimalgoritmo
