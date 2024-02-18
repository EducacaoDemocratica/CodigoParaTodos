# Exercício 33

[**Ver Análise**](Analise33.md)

```markdown
Algoritmo "Q33 - Vetor"
Var
  i, j, aux, lsup, lim: inteiro
  n, m: vetor [1..300] de inteiro

Inicio
  escreva("Insira a quantidade de funcionários: ")
  leia(lsup)

  enquanto ((lsup < 6) ou (lsup > 300)) faca
    escreva("A quantia deve ser de 6 a 300: ")
    leia (lsup)
  fimenquanto

  para i de 1 ate lsup faca
    escreva("Insira o identificador do", i,"º empregado: ")
    leia(n[i])

    enquanto (n[i] <= 0) faca
      escreva("Os identificadores devem ser maiores que 0: ")
      leia (n[i])
    fimenquanto

    j <- 1

    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (n[i] = n[j]) faca
          escreva("Esse identificador já foi usado: ")
          leia (n[i])

          enquanto (n[i] <= 0) faca
            escreva("Os identificadores devem ser maiores que 0: ")
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
      enquanto (m[i] = m[j]) faca
        escreva("Esse mês já foi usado: ")
        leia (m[i])

        enquanto (m[i] <= 0) faca
          escreva("Os meses devem ser maiores que 0: ")
          leia (m[i])
        fimenquanto
      fimenquanto
    fimse

    j <- j + 1
  fimenquanto

  escreval
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (m[i] > m[i + 1]) entao
        aux <- n[i]
        n[i] <- n[i + 1]
        n[i + 1] <- aux
        aux <- m[i]
        m[i] <- m[i + 1]
        m[i + 1] <- aux
      fimse
    fimpara
  fimpara

  lim <- 5
  escreval("Os", lim," empregados mais recentes: ")
  escreval

  para i de 1 ate lim faca
    escreval("Identificador:",n[i], " - Meses trabalhados:",m[i],".")
  fimpara

Fimalgoritmo
