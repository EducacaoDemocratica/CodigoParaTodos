# Exercício 21

[**Ver Análise**](Analise21.md)

```markdown
Algoritmo "Q21 - Vetor"
Var
  i, j, aux, p, lsup, x: inteiro
  a, b: vetor [1..30] de inteiro

Inicio
  lsup <- 30
  p <- -1

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º número de A: ")
    leia(a[i])
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (a[i] > a[i + 1]) entao
        aux <- a[i]
        a[i] <- a[i + 1]
        a[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º número de B: ")
    leia(b[i])
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (b[i] > b[i + 1]) entao
        aux <- b[i]
        b[i] <- b[i + 1]
        b[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval

  escreva("Insira o valor de x: ")
  leia(x)

  enquanto ((i <= lsup) e (p <> 0)) faca
    se (a[i] > x) entao
      p <- 0
    senao
      se (a[i] = x) entao
        p <- i
      fimse
    fimse
    i <- i + 1
  fimenquanto

  escreval

  escreva("Vetor A: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(a[i], ".")
    senao
      escreva(a[i], ",")
    fimse
  fimpara

  escreval

  escreva("Vetor B: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(b[i], ".")
    senao
      escreva(b[i], ",")
    fimse
  fimpara

  escreval

  se (p > 0) entao
    escreval(x, " está em A na", p, "ª posição.")
    escreval("O elemento na mesma posição em B é", b[p], ".")
  senao
    escreval(x, " não está em A.")
  fimse

Fimalgoritmo
