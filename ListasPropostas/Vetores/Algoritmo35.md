# Exercício 35

[**Ver Análise**](Analise35.md)

```markdown
Algoritmo "Q35 - Vetor"
Var
  i, lsup: inteiro
  a, b, c: vetor [1..8] de inteiro
Inicio
  lsup <- 8
  para i de 1 ate lsup faca
    escreva("Insira o",i,"º valor do vetor A: ")
    leia (a[i])
  fimpara
  escreval
  para i de 1 ate lsup faca
    escreva("Insira o",i,"º valor do vetor B: ")
    leia (b[i])
  fimpara
  escreval
  para i de 1 ate lsup faca
    c[i] <- a[i] * b[i]
  fimpara
  escreva("Vetor A:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(a[i], ".")
    senao
      escreva(a[i], ",")
    fimse
  fimpara
  escreva("Vetor B:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(b[i], ".")
    senao
      escreva(b[i], ",")
    fimse
  fimpara
  escreva("Vetor C:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(c[i], ".")
    senao
      escreva(c[i], ",")
    fimse
  fimpara
Fimalgoritmo
