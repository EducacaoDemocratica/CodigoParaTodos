# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - Vetor"
Var
  i, lsup, laux, aux: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o", i," número: ")
    leia(v[i])
  fimpara

  escreva("Vetor antes da inversão:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  laux <- lsup div 2

  para i de 1 ate laux faca
    aux <- v[i]
    v[i] <- v[lsup]
    v[lsup] <- aux
    lsup <- lsup - 1
  fimpara

  lsup <- lsup * 2

  escreva("Vetor depois da inversão:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

Fimalgoritmo
