# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown
Algoritmo "Q3 - Vetor"
Var
  i, lsup: inteiro
  h: vetor [1..10] de real
  m: real

Inicio
  lsup <- 10
  m <- 0

  escreval("Insira a altura em metros.")
  escreval

  para i de 1 ate lsup faca
    escreva("Insira a altura do ", i, "º atleta: ")
    leia(h[i])

    enquanto (h[i] <= 0) faca
      escreva("A altura deve ser maior que 0: ")
      leia(h[i])
    fimenquanto

  fimpara

  para i de 1 ate lsup faca
    m <- m + h[i]
  fimpara

  m <- m/i

  escreval
  escreval("A média das alturas inseridas é ", m:6:2, "m.")
  escreval("Atletas com altura acima da média: ")
  escreval

  para i de 1 ate lsup faca
    se (h[i] > m) entao
      escreval(i, "º atleta com ", h[i], "m.")
    fimse
  fimpara

Fimalgoritmo
