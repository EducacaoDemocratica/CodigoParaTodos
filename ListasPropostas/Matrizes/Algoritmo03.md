# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown
Algoritmo "Q3 - Matriz"

Var
  m, maux: vetor [1..3, 1..3] de inteiro
  i, j, p, lsup, aux, k: inteiro

Inicio
  lsup <- 3
  k <- 0

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      p <- j + ((i - 1) * 3)
      escreva("Insira o ", p,"º valor da matriz: ")
      leia(m[i, j])
    fimpara
  fimpara

  para i de lsup ate 1 passo -1 faca
    p <- 0
    k <- k + 1
    para j de 1 ate lsup faca
      p <- p + 1
      maux[k, p] <- m[j, i] // Note a inversão dos índices j e i aqui
    fimpara
  fimpara

  escreval
  escreval("Matriz original:")
  escreval
  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j], " ")
    fimpara
    escreval
  fimpara

  escreval
  escreval("Matriz após giro em 270º:")
  escreval
  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(maux[i, j], " ")
    fimpara
    escreval
  fimpara

Fimalgoritmo
