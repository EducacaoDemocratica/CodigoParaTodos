# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown
Algoritmo "Q20 - Matriz"
Var
  i, j, k, lsupl, lsups, aux: inteiro
  a: vetor [1..10, 1..10] de inteiro
  s: vetor [1..6] de inteiro
  acertos, tamanho: vetor [1..10] de inteiro

Inicio
  lsupl <- 10
  lsups <- 6

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
  fimenquanto

  para j de (lsups - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (s[i] > s[i + 1]) entao
        aux <- s[i]
        s[i] <- s[i + 1]
        s[i + 1] <- aux
      fimse
    fimenquanto
  fimenquanto

  para i de 1 ate lsupl faca
    escreva("Insira a quantidade de números da", i, " aposta: ")
    leia(tamanho[i])

    enquanto ((tamanho[i] < 6) ou (tamanho[i] > 10)) faca
      escreva("Faça a sua aposta de 6 a 10 números: ")
      leia(tamanho[i])
    fimenquanto

    escreval

    para j de 1 ate tamanho[i] faca
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
    fimenquanto

    escreval
  fimenquanto

  para k de 1 ate lsupl faca
    para j de (tamanho[k] - 1) ate 1 passo -1 faca
      para i de 1 ate j faca
        se (a[k, i] > a[k, i + 1]) entao
          aux <- a[k, i]
          a[k, i] <- a[k, i + 1]
          a[k, i + 1] <- aux
        fimse
      fimenquanto
    fimenquanto
  fimenquanto

  escreval

  para i de 1 ate lsupl faca
    para j de 1 ate tamanho[i] faca
      para k de 1 ate lsups faca
        se (a[i, j] = s[k]) entao
          acertos[i] <- acertos[i] + 1
        fimse
      fimenquanto
    fimenquanto
  fimenquanto

  escreval

  para i de 1 ate lsupl faca
    escreva(i,"ª aposta (", tamanho[i], " números): ")
    
    para j de 1 ate tamanho[i] faca
      se (j = tamanho[i]) entao
        escreval(a[i, j], ".")
      senao
        escreva(a[i, j], ",")
      fimse
    fimenquanto
  fimenquanto

  escreval

  escreva("Números sorteados: ")
  
  para i de 1 ate lsups faca
    se (i = lsups) entao
      escreval(s[i], ".")
    senao
      escreva(s[i], ",")
    fimse
  fimenquanto

  escreval

  para i de 1 ate lsupl faca
    escreval("A", i," aposta acertou", acertos[i]," número(s).")
  fimenquanto

Fimalgoritmo
