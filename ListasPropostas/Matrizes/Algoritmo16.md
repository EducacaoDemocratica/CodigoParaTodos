# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown
Algoritmo "Q16 - Matriz"
Var
  m: vetor [1..10, 1..10] de inteiro
  vh, vv, vd: vetor [1..4] de inteiro
  i, j, n, lsup, lsupVet, linha, coluna, diagonal: inteiro
  ph, pv, pd, aux: real
  principal: logico

Inicio
  lsup <- 10
  lsupVet <- 4

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      n <- j + ((i - 1) * lsup)
      escreva("Insira o", n, "º valor da matriz: ")
      leia(m[i, j])
    fimpara
  fimpara

  para i de 1 ate lsup faca
    para j de 1 ate (lsup - 3) faca
      aux <- m[i, j] * m[i, j + 1] * m[i, j + 2] * m[i, j + 3]
      se ((j = 1) e (i = 1)) entao
        ph <- aux
        linha <- i
        vh[1] <- m[i, j]
        vh[2] <- m[i, j + 1]
        vh[3] <- m[i, j + 2]
        vh[4] <- m[i, j + 3]
      senao
        se (aux > ph) entao
          ph <- aux
          linha <- i
          vh[1] <- m[i, j]
          vh[2] <- m[i, j + 1]
          vh[3] <- m[i, j + 2]
          vh[4] <- m[i, j + 3]
        fimse
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    para j de 1 ate (lsup - 3) faca
      aux <- m[j, i] * m[j + 1, i] * m[j + 2, i] * m[j + 3, i]
      se ((j = 1) e (i = 1)) entao
        pv <- aux
        coluna <- i
        vv[1] <- m[j, i]
        vv[2] <- m[j + 1, i]
        vv[3] <- m[j + 2, i]
        vv[4] <- m[j + 3, i]
      senao
        se (aux > pv) entao
          pv <- aux
          coluna <- i
          vv[1] <- m[j, i]
          vv[2] <- m[j + 1, i]
          vv[3] <- m[j + 2, i]
          vv[4] <- m[j + 3, i]
        fimse
      fimse
    fimpara
  fimpara

  principal <- verdadeiro

  para i de 1 ate (lsup - 3) faca
    para j de 1 ate (lsup - 3) faca
      aux <- m[j, i] * m[j + 1, i + 1] * m[j + 2, i + 2] * m[j + 3, i + 3]
      se ((j = 1) e (i = 1)) entao
        pd <- aux
        diagonal <- i
        vd[1] <- m[j, i]
        vd[2] <- m[j + 1, i + 1]
        vd[3] <- m[j + 2, i + 2]
        vd[4] <- m[j + 3, i + 3]
      senao
        se (aux > pd) entao
          pd <- aux
          diagonal <- i
          vd[1] <- m[j, i]
          vd[2] <- m[j + 1, i + 1]
          vd[3] <- m[j + 2, i + 2]
          vd[4] <- m[j + 3, i + 3]
        fimse
      fimse
    fimpara
  fimpara

  para i de lsup ate (1 + 3) passo - 1 faca
    para j de lsup ate (1 + 3) passo - 1 faca
      i - 3]
      aux <- m[j, i] * m[j - 1, i - 1] * m[j - 2, i - 2] * m[j - 3, i - 3]
      se (aux > pd) entao
        principal <- falso
        pd <- aux
        diagonal <- i
        vd[1] <- m[j, i]
        vd[2] <- m[j - 1, i - 1]
        vd[3] <- m[j - 2, i - 2]
        vd[4] <- m[j - 3, i - 3]
      fimse
    fimpara
  fimpara

  escreval
  escreval("Matriz: ")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j])
    fimpara
    escreval
  fimpara

  escreval

  escreval("Maior produto da horizontal se encontra na", linha, "ª linha:")
  escreva(ph, " =")

  para i de 1 ate lsupVet faca
    se (i = 1) entao
      escreva(vh[i])
    senao
      escreva(" *", vh[i])
    fimse
  fimpara

  escreval
  escreval

  escreval("Maior produto da vertical está na", coluna, "ª coluna:")
  escreva(pv, " =")

  para i de 1 ate lsupVet faca
    se (i = 1) entao
      escreva(vv[i])
    senao
      escreva(" *", vv[i])
    fimse
  fimpara

  escreval
  escreval

  escreva("Maior produto da diagonal está na", diagonal, "ª diagonal no sentido ")
  se (principal = verdadeiro) entao
    escreva("principal:")
  senao
    escreva("secundário:")
  fimse

  escreva(pd, " =")

  para i de 1 ate lsupVet faca
    se (i = 1) entao
      escreva(vd[i])
    senao
      escreva(" *", vd[i])
    fimse
  fimpara

  escreval
Fimalgoritmo
