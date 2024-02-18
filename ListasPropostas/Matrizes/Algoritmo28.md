# Exercício 28

[**Ver Análise**](Analise28.md)

```markdown
Algoritmo "Q28 - Matriz"

Var
  m: vetor [1..10, 1..10] de inteiro
  b, x: vetor [1..20] de real
  auxNum: real
  n, p, lsup, i, j: inteiro
  aux: caractere

Inicio
  p <- 0

  escreva("Insira o número de raízes: ")
  leia(n)

  enquanto ((n < 3) ou (n > 10)) faca
    escreva("Insira de 3 a 10 raízes: ")
    leia(n)
  fimenquanto

  escreval

  para i de 1 ate n faca
    para j de i ate n faca
      p <- p + 1
      escreva("Insira o", p, "º valor da matriz A: ")
      leia(m[i, j])
    fimpara
  fimpara

  escreval

  para i de 1 ate n faca
    escreva("Insira o", i, "º valor do vetor B dos termos independentes: ")
    leia(b[i])
  fimpara

  escreval
  escreval("SISTEMA FORMADO (n =", n, "): ")
  escreval

  para i de 1 ate n faca
    para j de 1 ate n faca
      se (j >= i) entao
        aux <- numpcarac(j)
        escreva(m[i, j], "X", aux, "")
      senao
        escreva("
")
      fimse
    fimpara
    escreval(" =", b[i])
  fimpara

  para i de n ate 1 passo -1 faca
    auxNum <- b[i]

    para j de n ate i passo -1 faca
      auxNum <- auxNum + (x[j] * m[i, j] * -1)
    fimpara

    se (m[i, i] <> 0) entao
      x[i] <- auxNum/m[i, i]
    senao
      x[i] <- 0
    fimse
  fimpara

  escreval
  escreval("RAÍZES DO SISTEMA: ")
  escreval

  para i de 1 ate n faca
    aux <- numpcarac(i)
    escreval("X", aux, ":", x[i])
  fimpara

Fimalgoritmo
