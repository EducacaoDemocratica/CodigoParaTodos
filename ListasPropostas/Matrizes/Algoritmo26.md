# Exercício 26

[**Ver Análise**](Analise26.md)

```markdown
Algoritmo "Q26 - Matriz"
Var
  m, mb: vetor [1..5, 1..5] de caractere
  i, j, l, n, c, latual, catual, cinicio, linf, lsup,
  lsupLinha, linfColuna, lsupColuna: inteiro
  perdeu, ganhou: logico
  linfLinha,
Inicio
  perdeu <- falso
  ganhou <- falso
  linf <- 1
  lsup <- 5

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      m[i, j] <- "*"
    fimpara
  fimpara

  cinicio <- randi(4) + 1
  m[lsup, cinicio] <- "J"
  latual <- lsup
  catual <- cinicio
  i <- 0

  enquanto (i < 7) faca
    c <- randi(4) + 1
    l <- randi(4) + 1
    se ((mb[l, c] = "") e ((c <> catual) e (l <> latual))) entao
      i <- i + 1
      mb[l, c] <- "BOMBA"
    fimse
  fimenquanto

  l <- randi(4) + 1

  enquanto ((perdeu = falso) e (ganhou = falso)) faca
    n <- 0
    escreval
    escreval
    escreval("1 2 3 4 5")

    para i de 1 ate lsup faca
      para j de 1 ate lsup faca
        se (j = 1) entao
          escreva(i," ")
        fimse
        escreva(m[i, j]," ")
      fimpara
      escreval
    fimpara

    se (latual = linf) entao
      linfLinha <- latual
      lsupLinha <- latual + 1
    senao
      se (latual = lsup) entao
        linfLinha <- latual - 1
        lsupLinha <- latual
      senao
        linfLinha <- latual - 1
        lsupLinha <- latual + 1
      fimse
    fimse

    se (catual = linf) entao
      linfColuna <- catual
      lsupColuna <- catual + 1
    senao
      se (catual = lsup) entao
        linfColuna <- catual - 1
        lsupColuna <- catual
      senao
        linfColuna <- catual - 1
        lsupColuna <- catual + 1
      fimse
    fimse

    para i de linfLinha ate lsupLinha faca
      para j de linfColuna ate lsupColuna faca
        se (mb[i, j] = "BOMBA") entao
          n <- n + 1
        fimse
      fimpara
    fimpara

    escreval
    escreval("Existem", n," bombas ao seu redor.")
    escreva("Insira uma linha: ")
    leia(l)

    enquanto ((l < linf) ou (l > lsup) ou (l < (latual - 1)) ou (l > (latual + 1))) faca
      escreva("Valor fora da vizinha ou além do tabuleiro. Insira outra linha: ")
      leia(l)
    fimenquanto

    escreva("Insira uma coluna: ")
    leia(c)

    enquanto ((c < linf) ou (c > lsup) ou (c < (catual - 1)) ou (c > (catual + 1))) faca
      escreva("Valor fora da vizinha ou além do tabuleiro. Insira outra coluna: ")
      leia(c)
    fimenquanto

    enquanto ((l = latual) e (c = catual)) faca
      escreva("Insira uma linha: ")
      leia(l)
      enquanto ((l < linf) ou (l > lsup) ou (l < (latual - 1)) ou (l > (latual + 1))) faca
        escreva("Valor fora da vizinha ou além do tabuleiro. Insira outra linha: ")
        leia(l)
      fimenquanto

      escreva("Insira uma coluna: ")
      leia(c)
    fimenquanto

    fimenquanto

    se (mb[l, c] = "BOMBA") entao
      perdeu <- verdadeiro
      m[l, c] <- "B"
    senao
      m[latual, catual] <- "X"
      m[l, c] <- "J"
      latual <- l
      catual <- c
      ganhou <- verdadeiro
      para i de 1 ate lsup faca
        para j de 1 ate lsup faca
          se ((m[i, j] = "*") e (mb[i, j] <> "BOMBA")) entao
            ganhou <- falso
          fimse
        fimpara
      fimpara

    se (ganhou = verdadeiro) entao
      para i de 1 ate lsup faca
        para j de 1 ate lsup faca
          se (m[i, j] = "*") entao
            m[i, j] <- "B"
          fimse
        fimpara
      fimpara
    fimse
  fimenquanto

  escreval
  escreval
  escreval("1 2 3 4 5")

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      se (j = 1) entao
        escreva(i," ")
      fimse
      escreva(m[i, j]," ")
    fimpara
    escreval
  fimpara

  escreval

  se (ganhou = verdadeiro) entao
    escreval("O JOGADOR VENCEU!")
  senao
    escreval("O JOGADOR PERDEU!")
  fimse

Fimalgoritmo
