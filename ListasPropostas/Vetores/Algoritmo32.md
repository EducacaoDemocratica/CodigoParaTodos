# Exercício 31

[**Ver Análise**](Analise31.md)

```markdown
Algoritmo "Q31 - Vetor"
Var
  i, j, aux, lsup: inteiro
  n, t: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  escreval("(Considere o tempo em segundos)")

  para i de 1 ate lsup faca
    escreva("Insira o número de inscrição do", i,"º atleta: ")
    leia(n[i])

    enquanto ((n[i] <= 0) ou (n[i] > 10)) faca
      escreva("Os números de inscrição vão de 1 a 10: ")
      leia (n[i])
    fimenquanto

    j <- 1

    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (n[i] = n[j]) faca
          escreva("Esse número já foi cadastrado: ")
          leia (n[i])

          enquanto ((n[i] <= 0) ou (n[i] > 10)) faca
            escreva("Os números de inscrição vão de 1 a 10: ")
            leia (n[i])
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto
  fimpara

  j <- 1

  enquanto (j < i) faca
    se (j <> i) entao
      enquanto (t[i] = t[j]) faca
        escreva("Esse tempo já foi cadastrado: ")
        leia (t[i])

        enquanto (t[i] <= 0) faca
          escreva("O tempo deve ser maior que 0: ")
          leia(t[i])
        fimenquanto
      fimenquanto
    fimse

    j <- j + 1
  fimenquanto

  escreval

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (t[i] > t[i + 1]) entao
        aux <- n[i]
        n[i] <- n[i + 1]
        n[i + 1] <- aux
        aux <- t[i]
        t[i] <- t[i + 1]
        t[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval("COLOCAÇÃO: ")
  escreval

  para i de 1 ate lsup faca
    escreval("Inscrição: Nº",n[i], " - Tempo", t[i],"s.")
  fimpara

Fimalgoritmo
