# Exercício 46

[**Ver Análise**](Analise46.md)

```markdown
Algoritmo "Q46 - Vetor"
Var
  i, j, lsups, lsupa, aux, acertos: inteiro
  s: vetor [1..6] de inteiro
  a: vetor [1..10] de inteiro

Inicio
  lsups <- 6
  acertos <- 0

  para i de 1 ate lsups faca
    s[i] <- (randi(59) + 1)
    j <- 1
    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (s[i] = s[j]) faca
          s[i] <- (randi(59) + 1)
          j <- 1
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  para j de (lsups - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (s[i] > s[i + 1]) entao
        aux <- s[i]
        s[i] <- s[i + 1]
        s[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreva("Insira a quantidade de números da sua aposta: ")
  leia(lsupa)
  escreval

  enquanto ((lsupa < 6) ou (lsupa > 10)) faca
    escreva("Insira de 6 a 10 números em sua aposta: ")
    leia(lsupa)
  fimenquanto

  escreval

  para i de 1 ate lsupa faca
    escreva("Insira o ", i,"º número da aposta: ")
    leia(a[i])

    enquanto ((a[i] <= 0) ou (a[i] > 60)) faca
      escreva("Insira valores de 1 a 60: ")
      leia(a[i])
    fimenquanto

    j <- 1
    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (a[i] = a[j]) faca
          escreva("Esse valor já está na aposta: ")
          leia (a[i])
          
          enquanto ((a[i] <= 0) ou (a[i] > 60)) faca
            escreva("Insira valores de 1 a 60: ")
            leia(a[i])
          fimenquanto
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto
  fimpara

  para j de (lsupa - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (a[i] > a[i + 1]) entao
        aux <- a[i]
        a[i] <- a[i + 1]
        a[i + 1] <- aux
      fimse
    fimpara
  fimpara

  para i de 1 ate lsupa faca
    para j de 1 ate lsups faca
      se (a[i] = s[j]) entao
        acertos <- acertos + 1
      fimse
    fimpara
  fimpara

  escreval
  escreva("Números sorteados: ")
  para i de 1 ate lsups faca
    se (i = lsups) entao
      escreval(s[i], ".")
    senao
      escreva(s[i], ",")
    fimse
  fimpara

  escreva("Números da aposta: ")
  para i de 1 ate lsupa faca
    se (i = lsupa) entao
      escreval(a[i], ".")
    senao
      escreva(a[i], ",")
    fimse
  fimpara

  escreval("O jogador acertou", acertos," dos", lsups," números sorteados.")
Fimalgoritmo
