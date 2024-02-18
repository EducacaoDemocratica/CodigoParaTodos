# Exercício 25

[**Ver Análise**](Analise25.md)

```markdown
Algoritmo "Q25 - Matriz"
Var
  m: vetor [1..3, 1..3] de caractere
  jog, comp: caractere
  i, j, l, n, c, k, lsup, aux, linha, coluna, diagonal: inteiro
  ganhou, jogou: logico

Inicio
  ganhou <- falso
  lsup <- 3
  k <- 0

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      m[i, j] <- "#"
    fimpara
  fimpara

  escreva("Escolha seu símbolo (X ou O): ")
  leia(jog)
  jog <- maiusc(jog)

  enquanto ((jog <> "X") e (jog <> "O")) faca
    escreva("Escolha X ou O: ")
    leia(jog)
    jog <- maiusc(jog)
  fimenquanto

  se (jog = "X") entao
    comp <- "O"
  senao
    comp <- "X"
  fimse

  escreval("Jogador: ", jog)
  escreval("Computador: ", comp)
  escreval

  enquanto ((k < (lsup * lsup)) e (ganhou = falso)) faca
    k <- k + 1
    escreval("Tabuleiro ")
    escreval

    para i de 1 ate lsup faca
      para j de 1 ate lsup faca
        escreva(m[i, j], " ")
      fimpara
      escreval
    fimpara

    escreval

    se (k mod 2 = 1) entao
      escreval("Vez do jogador (", jog, ").")
      escreval
      escreva("Selecione uma linha: ")
      leia(l)

      enquanto ((l < 1) ou (l > 3)) faca
        escreva("Selecione a 1ª, 2ª ou 3ª linha: ")
        leia(l)
      fimenquanto

      aux <- 0

      para j de 1 ate lsup faca
        se (m[l, j] <> "#") entao
          aux <- aux + 1
        fimse
      fimpara

      enquanto (aux = 3) faca
        escreva("Essa linha já está ocupada: ")
        leia(l)

        enquanto ((l < 1) ou (l > 3)) faca
          escreva("Selecione a 1ª, 2ª ou 3ª linha: ")
          leia(l)
        fimenquanto

        aux <- 0

        para j de 1 ate lsup faca
          se (m[l, j] <> "#") entao
            aux <- aux + 1
          fimse
        fimpara

      fimenquanto
      escreva("Selecione uma coluna: ")
      leia(c)

      enquanto ((c < 1) ou (c > 3)) faca
        escreva("Selecione a 1ª, 2ª ou 3ª coluna: ")
        leia(c)
      fimenquanto

      aux <- 0

      para j de 1 ate lsup faca
        se (m[j, c] <> "#") entao
          aux <- aux + 1
        fimse
      fimpara

      enquanto (aux = 3) faca
        escreva("Essa coluna já está ocupada: ")
        leia(c)

        enquanto ((c < 1) ou (c > 3)) faca
          escreva("Selecione a 1ª, 2ª ou 3ª coluna: ")
          leia(c)
        fimenquanto

        aux <- 0

        para j de 1 ate lsup faca
          se (m[j, c] <> "#") entao
            aux <- aux + 1
          fimse
        fimpara

      fimenquanto
      enquanto (m[l, c] <> "#") faca
        escreval("Essa posição já está ocupada. Insira outra.")
        escreva("Selecione uma linha: ")
        leia(l)

        enquanto ((l < 1) ou (l > 3)) faca
          escreva("Selecione a 1ª, 2ª ou 3ª linha: ")
          leia(l)
        fimenquanto

        aux <- 0

        para j de 1 ate lsup faca
          se (m[l, j] <> "#") entao
            aux <- aux + 1
          fimse
        fimpara

        enquanto (aux = 3) faca
          escreva("Essa linha já está ocupada: ")
          leia(l)

          enquanto ((l < 1) ou (l > 3)) faca
            escreva("Selecione a 1ª, 2ª ou 3ª linha: ")
            leia(l)
          fimenquanto

          aux <- 0

          para j de 1 ate lsup faca
            se (m[l, j] <> "#") entao
              aux <- aux + 1
            fimse
          fimpara

        fimenquanto
        escreva("Selecione uma coluna: ")
        leia(c)

        enquanto ((c < 1) ou (c > 3)) faca
          escreva("Selecione a 1ª, 2ª ou 3ª coluna: ")
          leia(c)
        fimenquanto

        aux <- 0

        para j de 1 ate lsup faca
          se (m[j, c] <> "#") entao
            aux <- aux + 1
          fimse
        fimpara

        enquanto (aux = 3) faca
          escreva("Essa coluna já está ocupada: ")
          leia(c)

          enquanto ((c < 1) ou (c > 3)) faca
            escreva("Selecione a 1ª, 2ª ou 3ª coluna: ")
            leia(c)
          fimenquanto

          aux <- 0

          para j de 1 ate lsup faca
            se (m[j, c] <> "#") entao
              aux <- aux + 1
            fimse
          fimpara

        fimenquanto
      fimenquanto
    senao
      jogou <- falso
      escreval("Vez do computador(", comp, ").")
      linha <- 0

      para i de 1 ate lsup faca
        n <- 1

        para j de 1 ate (lsup - 1) faca
          se (m[i, j] = jog) entao
            se (m[i, j] = m[i, j + 1]) entao
              n <- n + 1
            fimse
          fimse
        fimpara

        se (n = 2) entao
          linha <- i
        fimse
      fimpara

      se (linha <> 0) entao
        j <- 0

        enquanto ((j < lsup) e (jogou = falso)) faca
          j <- j + 1

          se (m[linha, j] = "#") entao
            m[linha, j] := comp
            jogou := verdadeiro
          fimse
        fimenquanto
      fimse

      se (jogou = falso) entao
        coluna := 0

        para i de 1 ate lsup faca
          n := 1

          para j de 1 ate (lsup - 1) faca
            se (m[j, i] = jog) entao
              se (m[j, i] = m[j + 1, i]) entao
                n := n + 1
              fimse
            fimse
          fimpara

          se (n = 2) entao
            coluna := i
          fimse
        fimpara

        se (coluna <> 0) entao
          j := 0

          enquanto ((j < lsup) e (jogou = falso)) faca
            j := j + 1

            se (m[j, coluna] = "#") entao
              m[j, coluna] := comp
              jogou := verdadeiro
            fimse
          fimenquanto
        fimse
      fimse

      se (jogou = falso) entao
        diagonal := 0

        para i de 1 ate (lsup - 1) faca
          n := 1

          se (m[i, i] = jog) entao
            se (m[i, i] = m[i + 1, i + 1]) entao
              n := n + 1
            fimse
          fimse
        fimpara

        se (n = 2) entao
          i := 0

          enquanto ((i < lsup) e (jogou = falso)) faca
            i := i + 1

            se (m[i, i] = "#") entao
              m[i, i] := comp
              jogou := verdadeiro
            fimse
          fimenquanto
        senao
          se ((m[3, 1] = jog) ou (m[2, 2] = jog) ou (m[1, 3] = jog)) entao
            se ((m[3, 1] = m[2, 2]) ou (m[3, 1] = m[1, 3]) ou (m[2, 2] = m[1, 3])) entao
              i := 0

              enquanto ((i < lsup) e (jogou = falso)) faca
                i := i + 1
                j := 0

                enquanto ((j < lsup) e (jogou = falso)) faca
                  j := j + 1

                  se ((i + j = lsup + 1) e (m[i, j] = "#")) entao
                    m[i, j] := comp
                    jogou := verdadeiro
                  fimse
                fimenquanto
              fimenquanto
            fimse
          fimse
        fimse
      fimse
    fimse
  fimenquanto

  escreval("Resultado ")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j], " ")
    fimpara
    escreval
  fimpara

  escreval

  se (k = 9) entao
    escreval("Empate!")
  senao
    se (k mod 2 = 1) entao
      escreval("O jogador (", jog, ") venceu!")
    senao
      escreval("O computador (", comp, ") venceu!")
    fimse
  fimse

Fimalgoritmo
