# Exercício 55

[**Ver Análise**](Analise55.md)

```markdown
Algoritmo "Q55 - Vetor"
Var
  lsup, i, k, j, achou: inteiro
  s: real
  n: vetor [1..30] de inteiro
  parou: logico

Inicio
  lsup <- 30
  i <- 0
  parou <- falso

  enquanto (i < lsup) e (parou = falso) faca
    i <- i + 1
    escreva("Insira um número: ")
    leia (n[i])

    enquanto (n[i] < 0) e (n[i] <> -1) faca
      escreva("Não insira números negativos: ")
      leia (n[i])
    fimenquanto

    se (n[i] = -1) entao
      parou <- verdadeiro
      n[i] <- 0
    senao
      se (n[i] = 0) entao
        achou <- 0
        j <- 1

        enquanto (j < i) faca
          se (n[j] <> 0) entao
            achou <- 1
          fimse
          j <- j + 1
        fimenquanto

        se (achou = 0) entao
          enquanto (n[i] = 0) faca
            escreval("Não há números para serem corrigidos!")
            escreva("Insira um valor diferente de 0: ")
            leia (n[i])
          fimenquanto
        senao
          j <- lsup

          enquanto (n[j] = 0) faca
            j <- j - 1
          fimenquanto

          n[j] <- 0
        fimse
      fimse
    fimse
  fimenquanto

  para j de 1 ate (i - 1) faca
    se (n[j] = 0) entao
      k <- j + 1
      enquanto ((n[k] = 0) e (k < lsup)) faca
        k <- k + 1
      fimenquanto

      n[j] <- n[k]
      n[k] <- 0
    fimse
    s <- s + n[j]
  fimpara

  escreval
  escreva("Números após correção:")

  i <- 1
  enquanto ((n[i] <> 0) e (i < lsup)) faca
    se (n[i + 1] = 0) entao
      escreval(n[i], ".")
    senao
      escreva(n[i], ",")
    fimse
    i <- i + 1
  fimenquanto

  escreval("Soma:", s,".")
Fimalgoritmo
