# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown
Algoritmo "Q13 - Matriz"
Var
  m: vetor [1..10, 1..10] de inteiro
  d: vetor [1..100] de real
  i, j, k, p, lsup, menor, maior: inteiro
  media, va, dp, s: real

Inicio
  lsup <- 10
  media <- 0
  va <- 0
  s <- 0

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      p <- j + ((i - 1) * lsup)
      escreva("Insira o", p, "º valor da matriz: ")
      leia(m[i, j])
    fimpara
  fimpara

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      se ((j = 1) e (i = 1)) entao
        menor <- m[i, j]
        maior <- m[i, j]
      senao
        se (m[i, j] > maior) entao
          maior <- m[i, j]
        fimse
        se (m[i, j] < menor) entao
          menor <- m[i, j]
        fimse
      fimse

      s <- s + m[i, j]
    fimpara
  fimpara

  media <- s / (i * j)

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      p <- j + ((i - 1) * lsup)
      d[i] <- m[i, j] - media
    fimpara
  fimpara

  para i de 1 ate lsup * lsup faca
    va <- va + (d[i] ^ 2)
  fimpara

  va <- va / i
  dp <- (va ^ (1/2))

  escreval
  escreval("Matriz:")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j])
    fimpara
    escreval
  fimpara

  escreval
  escreval("Soma dos elementos:", s, ".")
  escreval("Média:", media:6:2, ".")
  escreval("Variância:", va:6:2, ".")
  escreval("Desvio padrão:", dp:6:2, ".")
  escreval("Maior elemento:", maior, ".")
  escreval("Menor elemento:", menor, ".")

Fimalgoritmo
