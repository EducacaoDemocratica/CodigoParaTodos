# Exercício 53

[**Ver Análise**](Analise53.md)

```markdown
Algoritmo "Q53 - Vetor"
Var
  lsup, i, j, n: inteiro
  a: vetor[1..21] de inteiro
  p: vetor[1..10] de real
  x: vetor[1..10] de inteiro

Inicio
  lsup <- 10
  escreva("Insira um número: ")
  leia(n)

  enquanto (n <= 0) ou (n > 21) faca
    escreva("O número deve estar entre 1 e 21: ")
    leia(n)
  fimenquanto

  escreval

  para i de 1 ate n faca
    a[i] <- randi(99) + 1
  fimpara

  para i de 1 ate lsup faca
    escreva("Insira o ", i,"º valor para x: ")
    leia(x[i])

    para j de n ate 1 passo -1 faca
      p[i] <- p[i] + a[j] * (x[i]^j)
    fimpara
  fimpara

  escreval

  para i de 1 ate lsup faca
    escreval("Para x =", x[i],", P =", p[i],".")
  fimpara
Fimalgoritmo
