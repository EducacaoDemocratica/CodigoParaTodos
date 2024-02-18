# Exercício 30

[**Ver Análise**](Analise30.md)

```markdown
Algoritmo "Q30 - Vetor"
Var
  i, j, k, lsup, auxMaior, auxQ: inteiro
  q: vetor [1..9] de inteiro
  p: vetor [1..9] de real
  n, nMaior: vetor [1..9] de caractere
  auxN: caractere
  auxP: real

Inicio
  lsup <- 9

  para i de 1 ate lsup faca
    escreva("Insira o nome do", i, "º produto: ")
    leia(n[i])

    enquanto (n[i] = "") faca
      escreva("Preencha esse campo: ")
      leia (n[i])
    fimenquanto

    n[i] <- minusc(n[i])
    j <- 1

    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (n[i] = n[j]) faca
          escreva("Esse nome já está no cadastrado: ")
          leia (n[i])

          enquanto (n[i] = "") faca
            escreva("Preencha esse campo: ")
            leia (n[i])
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto
  fimpara

  j <- 1
  escreva("Insira o preço do", i, "º produto: ")
  leia(p[i])

  enquanto (p[i] <= 0) faca
    escreva("O preço deve ser maior que 0: ")
    leia(p[i])
  fimenquanto

  escreva("Insira a quantidade vendida do", i, "º produto: ")
  leia(q[i])

  enquanto (q[i] < 0) faca
    escreva("A quantidade vendida não pode ser negativa: ")
    leia(q[i])
  fimenquanto

  escreval
  fimpara

  escreval

  para i de 1 ate lsup faca
    se (i = 1) entao
      k <- 1
      auxMaior <- q[i]
      nMaior[k] <- n[i]
    senao
      se (q[i] > auxMaior) entao
        k <- 1
        auxMaior <- q[i]
        nMaior[k] <- n[i]
      senao
        se (q[i] = auxMaior) entao
          k <- k + 1
          nMaior[k] <- n[i]
        fimse
      fimse
    fimse
  fimpara

  escreva("nomes: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(n[i], ".")
    senao
      escreva(n[i], ",")
    fimse
  fimpara

  escreva("preços: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(p[i], ".")
    senao
      escreva(p[i], ",")
    fimse
  fimpara

  escreva("vendas: ")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(q[i], ".")
    senao
      escreva(q[i], ",")
    fimse
  fimpara

  escreval

  escreva("Produto(s) mais vendido(s): ")
  para i de 1 ate k faca
    se (i = k) entao
      escreval(nMaior[i], ".")
    senao
      escreva(nMaior[i], ",")
    fimse
  fimpara

  escreval

  escreval("Produtos e preços em ordem alfabética:")
  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (n[i] > n[i + 1]) entao
        auxN <- n[i]
        n[i] <- n[i + 1]
        n[i + 1] <- auxN
        auxQ <- q[i]
        q[i] <- q[i + 1]
        q[i + 1] <- auxQ
        auxP <- p[i]
        p[i] <- p[i + 1]
        p[i + 1] <- auxP
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    escreval(n[i], " - R$", p[i],".")
  fimpara

  escreval

  escreval("Produtos e vendas em ordem crescente de venda:")
  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (q[i] > q[i + 1]) entao
        auxN <- n[i]
        n[i] <- n[i + 1]
        n[i + 1] <- auxN
        auxQ <- q[i]
        q[i] <- q[i + 1]
        q[i + 1] <- auxQ
        auxP <- p[i]
        p[i] <- p[i + 1]
        p[i + 1] <- auxP
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    escreval(n[i], " -", q[i]," vendas.")
  fimpara

Fimalgoritmo
