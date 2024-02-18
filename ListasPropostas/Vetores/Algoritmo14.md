# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown
Algoritmo "Q14 - Vetor"
Var
  i, j, lsup, aux: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o",i,"º valor do vetor: ")
    leia (v[i])
    enquanto (v[i] <= 0) faca
      escreva("Insira valores maiores que 0: ")
      leia (v[i])
    fimenquanto
  fimpara

  escreval

  escreva("Antes da ordenação:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
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

  escreva("Pós ordenação em ordem crescente:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

Fimalgoritmo
