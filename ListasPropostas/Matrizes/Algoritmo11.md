# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown
Algoritmo "Q11 - Matriz"
Var
  m: vetor [1..2, 1..2] de inteiro
  mi: vetor [1..2, 1..2] de real
  i, j, p, lsup, det, ds, dp: inteiro

Inicio
  lsup <- 2
  ds <- 1
  dp <- 1
  det <- 0

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      p <- j + ((i - 1) * lsup)
      escreva("Insira o", p, "º valor da matriz: ")
      leia(m[i, j])
    fimpara
  fimpara

  para j de 1 ate lsup faca
    para i de 1 ate lsup faca
      se (i = j) entao
        dp <- dp * m[i, j]
      fimse
      se ((i + j) = (lsup + 1)) entao
        ds <- ds * m[i, j]
      fimse
    fimpara
  fimpara

  det <- dp - ds
  escreval

  escreval("Matriz original:")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j])
    fimpara
    escreval
  fimpara

  escreval

  se (det = 0) entao
    escreval("A matriz não possui inversa.")
  senao
    mi[2, 2] <- m[1, 1]
    mi[1, 1] <- m[2, 2]
    mi[1, 2] <- (m[1, 2] * -1)
    mi[2, 1] <- (m[2, 1] * -1)

    para j de 1 ate lsup faca
      para i de 1 ate lsup faca
        mi[i, j] <- mi[i, j] * (1/det)
      fimpara
    fimpara

    escreval("Matriz inversa:")
    escreval

    para i de 1 ate lsup faca
      para j de 1 ate lsup faca
        escreva(mi[i, j]:6:2)
      fimpara
      escreval
    fimpara
  fimse

Fimalgoritmo
