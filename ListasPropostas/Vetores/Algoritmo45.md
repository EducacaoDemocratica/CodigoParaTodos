# Exercício 45

[**Ver Análise**](Analise45.md)

```markdown
Algoritmo "Q45 - Vetor"
Var
  i, j, lsup, aux: inteiro
  s: vetor [1..6] de inteiro

Inicio
  lsup <- 6

  para i de 1 ate lsup faca
    s[i] <- (randi(59) + 1)
    j <- 1
    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (s[i] = s[j]) faca
          s[i] <- (randi(59) + 1)
          j <- 1
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (s[i] > s[i + 1]) entao
        aux <- s[i]
        s[i] <- s[i + 1]
        s[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval
  escreva("Números sorteados: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(s[i], ".")
    senao
      escreva(s[i], ",")
    fimse
  fimpara
Fimalgoritmo
