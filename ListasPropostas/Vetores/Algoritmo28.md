# Exercício 28

[**Ver Análise**](Analise28.md)

```markdown
Algoritmo "Q28 - Vetor"
Var
  i, lsup, t, k, j, auxmenor, auxmaior: inteiro
  q, maior, menor: vetor [1..9] de inteiro

Inicio
  lsup <- 9
  t <- 0

  para i de 1 ate lsup faca
    escreva("Insira a quantidade vendida do", i, "º produto: ")
    leia(q[i])

    enquanto (q[i] < 0) faca
      escreva("A quantidade vendida não pode ser negativa: ")
      leia(q[i])
    fimenquanto
  fimpara

  para i de 1 ate lsup faca
    t <- t + q[i]

    se (i = 1) entao
      k <- 1
      j <- 1
      auxmaior <- q[i]
      auxmenor <- q[i]
      maior[k] <- i
      menor[j] <- i
    senao
      se (q[i] > auxmaior) entao
        k <- 1
        auxmaior <- q[i]
        maior[k] <- i
      senao
        se (q[i] = auxmaior) entao
          k <- k + 1
          maior[k] <- i
        fimse
      fimse

      se (q[i] < auxmenor) entao
        j <- 1
        auxmenor <- q[i]
        menor[j] <- i
      senao
        se (q[i] = auxmenor) entao
          j <- j + 1
          menor[j] <- i
        fimse
      fimse
    fimse
  fimpara

  escreval
  escreval("Total vendido:", t)
  escreva("Produto(s) mais vendido(s):")

  para i de 1 ate k faca
    se (i = k) entao
      escreval(maior[i], "º.")
    senao
      escreva(maior[i], "/º,")
    fimse
  fimpara

  escreva("Produto(s) menos vendido(s):")

  para i de 1 ate j faca
    se (i = j) entao
      escreval(menor[i], "º.")
    senao
      escreva(menor[i], "º,")
    fimse
  fimpara

Fimalgoritmo
