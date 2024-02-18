# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown
Algoritmo "Q9 - Vetor"
Var
  i, lsup, s, n: inteiro
  v: vetor [1..10] de inteiro

Inicio
  lsup <- 10

  escreva("Insira um número: ")
  leia(n)

  enquanto ((n <= 0) ou (n > lsup)) faca
    escreva("Insira um número maior que 0 e menor/igual a 10: ")
    leia(n)
  fimenquanto

  lsup <- n

  para i de 1 ate lsup faca
    escreva("Insira o", i,"º número: ")
    leia(v[i])

    enquanto (v[i] <= 0) faca
      escreva("Insira um número maior que 0: ")
      leia(v[i])
    fimenquanto
  fimpara

  escreval

  para i de 1 ate lsup faca
    s <- s + v[i]
  fimpara

  escreval("Média dos valores inseridos: ", s/i)

Fimalgoritmo
