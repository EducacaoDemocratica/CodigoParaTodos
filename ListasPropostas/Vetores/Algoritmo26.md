# Exercício 26

[**Ver Análise**](Analise26.md)

```markdown
Algoritmo "Q26 - Vetor"
Var
  i, lsup, j, aux: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreva("Insira o",i,"º valor do vetor: ")
    leia (v[i])
    j <- 1

    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (v[i] = v[j]) faca
          escreva("Esse valor já está no vetor: ")
          leia (v[i])
          j <- 1
        fimenquanto
      fimse
      j <- j + 1
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

  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

Fimalgoritmo
