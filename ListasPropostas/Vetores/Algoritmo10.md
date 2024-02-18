# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown
Algoritmo "Q10 - Vetor"
Var
  i, lsup, s, n: inteiro
  v: vetor [1..10] de inteiro
  negativo: logico

Inicio
  lsup <- 10
  negativo <- falso

  escreva("Insira um número: ")
  leia(n)

  enquanto ((n <= 0) ou (n > lsup)) faca
    escreva("Insira um número maior que 0 e menor/igual a 10: ")
    leia(n)
  fimenquanto

  lsup <- n
  i <- 1

  enquanto ((i <= lsup) e negativo = falso) faca
    escreva("Insira o", i,"º número: ")
    leia(v[i])

    se (v[i] < 0) entao
      negativo <- verdadeiro
      v[i] <- 0
    senao
      i <- i + 1
    fimse
  fimenquanto

  lsup <- i - 1

  para i de 1 ate lsup faca
    s <- s + v[i]
  fimpara

  escreval("Média dos valores inseridos: ", s/i)

Fimalgoritmo
