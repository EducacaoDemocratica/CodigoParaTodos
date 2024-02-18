# Exercício 54

[**Ver Análise**](Analise54.md)

```markdown
Algoritmo "Q54 - Vetor"
Var
  i, j, n, lim, lsup, linfr, lsupr, scomp, sjog, aux, dcomp, djog, p: inteiro
  r: vetor [2..10] de inteiro
  jog, comp: vetor [1..3] de inteiro

Inicio
  lim <- 4
  linfr <- 2
  lsupr <- 10
  lsup <- 3
  scomp <- 0
  sjog <- 0

  para i de 1 ate lsup faca
    comp[i] <- randi(8) + 2
  fimpara

  para i de linfr ate lsupr faca
    para j de 1 ate lsup faca
      se(comp[j] = i) entao
        r[i] <- r[i] + 1
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    jog[i] <- randi(8) + 2
    j <- linfr
    enquanto (j < lsupr) faca
      se (jog[i] = j) entao
        se (r[j] <> lim) entao
          r[j] <- r[j] + 1
        senao
          jog[i] <- randi(8) + 2
          j <- (linfr - 1)
        fimse
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  escreva("Cartas do jogador: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(jog[i],".")
    senao
      escreva(jog[i],",")
    fimse
  fimpara

  escreval("Deseja trocar quantas cartas?")
  escreva("Selecione 0, 1 ou 2: ")
  leia(n)

  enquanto ((n < 0) ou (n > 2)) faca
    escreva("Selecione 0, 1 ou 2: ")
    leia(n)
  fimenquanto

  escreval

  para i de 1 ate n faca
    escreva("Qual carta você gostaria de trocar: ")
    leia(aux)
    p <- 0

    para j de 1 ate lsup faca
      se (aux = jog[j]) entao
        p <- j
      fimse
    fimpara

    enquanto (p = 0) faca
      escreval("Você não possui essa carta.")
      escreva("Insira outra: ")
      leia(aux)
      p <- 0

      para j de 1 ate lsup faca
        se (aux = jog[j]) entao
          p <- j
        fimse
      fimpara
    fimenquanto

    enquanto (aux = jog[p]) faca
      jog[p] <- randi(8) + 2
      j <- linfr

      enquanto (j < lsupr) faca
        se (jog[p] = j) entao
          se (r[j] <> lim) entao
            r[j] <- r[j] + 1
          senao
            jog[p] <- randi(8) + 2
            j <- (linfr - 1)
          fimse
        fimse
        j <- j + 1
      fimenquanto
    fimenquanto

    escreval("Carta trocada:", aux," ->", jog[p],".")
    escreval
  fimpara

  para i de 1 ate lsup faca
    scomp <- scomp + comp[i]
    sjog <- sjog + jog[i]
  fimpara

  dcomp <- 21 - scomp
  djog <- 21 - sjog

  se (dcomp < 0) entao
    dcomp <- dcomp * (-1)
  fimse

  se (djog < 0) entao
    djog <- djog * (-1)
  fimse

  escreva("Baralho do jogador: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(jog[i],".")
    senao
      escreva(jog[i],",")
    fimse
  fimpara

  escreval("Soma do jogador:", sjog,".")
  escreval

  escreva("Baralho do computador: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(comp[i],".")
    senao
      escreva(comp[i],",")
    fimse
  fimpara

  escreval("Soma do computador:", scomp,".")
  escreval

  se (djog < dcomp) entao
    escreval("O jogador venceu!")
  senao
    se (dcomp < djog) entao
      escreval("O computador venceu!")
    senao
      escreval("Empate!")
    fimse
  fimse
Fimalgoritmo
