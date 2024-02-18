# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - Vetor"
Var
  i, aux, lsup: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    v[i] <- i
  fimpara

  escreval

  aux <- lsup div 2

  para i de 1 ate aux faca
    escreval(i,"ª posição +", lsup,"ª posição: ", v[i]," +", v[lsup]," =", v[i] + v[lsup])
    lsup <- lsup - 1
  fimpara

Fimalgoritmo
