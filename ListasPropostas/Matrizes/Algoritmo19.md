# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - Matriz"
Var
  i, j, k, lsupl, lsupc, aux: inteiro
  a: vetor [1..5, 1..6] de inteiro

Inicio
  lsupl <- 5
  lsupc <- 6

  para i de 1 ate lsupl faca
    para j de 1 ate lsupc faca
      escreva("Insira o ", j, "º número da", i, "ª aposta: ")
      leia(a[i, j])

      enquanto ((a[i, j] <= 0) ou (a[i, j] > 60)) faca
        escreva("Insira valores de 1 a 60: ")
        leia(a[i, j])
      fimenquanto

      k <- 1
      enquanto (k < j) faca
        se (k <> j) entao
          enquanto (a[i, j] = a[i, k]) faca
            escreva("Esse valor já está na aposta: ")
            leia (a[i, j])
            enquanto ((a[i, j] <= 0) ou (a[i, j] > 60)) faca
              escreva("Insira valores de 1 a 60: ")
              leia(a[i, j])
            fimenquanto
          fimenquanto
        fimse
        k <- k + 1
      fimenquanto
    fimpara

    escreval
  fimpara

  para k de 1 ate lsupl faca
    para j de (lsupc - 1) ate 1 passo -1 faca
      para i de 1 ate j faca
        se (a[k, i] > a[k, i + 1]) entao
          aux <- a[k, i]
          a[k, i] <- a[k, i + 1]
          a[k, i + 1] <- aux
        fimse
      fimpara
    fimpara
  fimpara

  escreval

  para i de 1 ate lsupl faca
    escreva("Números da", i, "ª aposta: ")
    para j de 1 ate lsupc faca
      se (j = lsupc) entao
        escreval(a[i, j], ".")
      senao
        escreva(a[i, j], ",")
      fimse
    fimpara
  fimpara

Fimalgoritmo
