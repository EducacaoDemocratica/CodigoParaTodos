# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown
Algoritmo "Q15 - Matriz"
Var
  m: vetor [1..20, 1..20] de inteiro
  lsup, i, j: inteiro

Inicio
  escreva("Insira a quantidade de linhas do triângulo de Pascal: ")
  leia(lsup)

  enquanto ((lsup <= 0) ou (lsup > 20)) faca
    escreva("Insira valores de 1 até 20: ")
    leia(lsup)
  fimenquanto

  m[1, 1] <- 1

  para i de 2 ate lsup faca
    m[i, 1] <- 1
    m[1, i] <- 0

    para j de 2 ate lsup faca
      m[i, j] <- m[i - 1, j] + m[i - 1, j - 1]
    fimpara
  fimpara

  escreval
  escreval("Triângulo de Pascal gerado:")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      se (m[i, j] <> 0) entao
        escreva(m[i, j])
      senao
        escreva(" ")
      fimse
    fimpara
    escreval
  fimpara

Fimalgoritmo
