# Exercício 24

[**Ver Análise**](Analise24.md)

```markdown
Algoritmo "Q24 - Matriz"
Var
  m: vetor [1..3, 1..3] de caractere
  s1, s2, auxs: caractere
  i, j, l, c, k, lsup, aux: inteiro
  ganhou: logico

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
  leia(s1)
  s1 <- maiusc(s1)

  enquanto ((s1 <> "X") e (s1 <> "O")) faca
    escreva("Escolha X ou O: ")
    leia(s1)
    s1 <- maiusc(s1)
  fimenquanto

  se (s1 = "X") entao
    s2 <- "O"
  senao
    s2 <- "X"
  fimse

  escreval("Jogador 1: ", s1)
  escreval("Jogador 2: ", s2)

  enquanto ((k < (lsup * lsup)) e (ganhou = falso)) faca
    k <- k + 1
    escreval("Tabuleiro ")
    escreval

    para i de 1 ate lsup faca
      para j de 1 ate lsup faca
        escreva(m[i, j]," ")
      fimpara
      escreval
    fimpara

    escreval

    se (k mod 2 = 1) entao
      auxs <- s1
      escreval("Vez do primeiro jogador (", s1,").")
    senao
      auxs <- s2
      escreval("Vez do segundo jogador (", s2,").")
    fimse

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

    enqunato (m[l, c] <> "#") faca
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

    m[l, c] <- auxs

    para i de 1 ate lsup faca
      se (m[i, 1] <> "#") entao
        se ((m[i, 1] = m[i, 2]) e (m[i, 2] = m[i, 3])) entao
          ganhou <- verdadeiro
        fimse
      fimse
    fimpara

    se (ganhou = falso) entao
      para i de 1 ate lsup faca
        se (m[1, i] <> "#") entao
          se ((m[1, i] = m[2, i]) e (m[2, i] = m[3, i])) entao
            ganhou <- verdadeiro
          fimse
        fimse
      fimpara
    fimse

    se (ganhou = falso) entao
      i <- 1
      se (m[i, i] <> "#") entao
        se ((m[i, i] = m[i + 1, i + 1]) e (m[i + 1, i + 1] = m[i + 2, i + 2])) entao
          ganhou <- verdadeiro
        fimse
      fimse
    fimse

    se (ganhou = falso) entao
      i <- 1
      se (m[i, lsup] <> "#") entao
        se ((m[i, lsup] = m[i + 1, lsup - 1]) e (m[i + 1, lsup - 1] = m[i + 2, lsup - 2])) entao
          ganhou <- verdadeiro
        fimse
      fimse
    fimse
  fimenquanto

  escreval
  escreval("Resultado ")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j]," ")
    fimpara
    escreval
  fimpara

  escreval

  se (k = 9) entao
    escreval("Empate!")
  senao
    se (k mod 2 = 1) entao
      escreval("O jogador 1 (", s1,") venceu!")
    senao
      escreval("O jogador 2 (", s2,") venceu!")
    fimse
  fimse

Fimalgoritmo
