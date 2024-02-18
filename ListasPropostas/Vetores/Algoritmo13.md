# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown
Algoritmo "Q13 - Vetor"
Var
  n, i, lsup, c: inteiro
  v: vetor [1..10] de inteiro
  presente: logico

Inicio
  c <- 0
  lsup <- 10
  presente <- falso

  para i de 1 ate lsup faca
    escreva("Insira o",i,"º valor do vetor: ")
    leia (v[i])
  fimpara

  escreval

  escreva("Insira um número: ")
  leia (n)

  escreval

  para i de 1 ate lsup faca
    se (n = v[i]) entao
      presente <- verdadeiro
      c <- c + 1
    fimse
  fimpara

  se (presente = verdadeiro) entao
    escreval(n, " está presente na estrutura e aparece", c, " vezes.")
  senao
    escreval(n, " não está presente na estrutura.")
  fimse

Fimalgoritmo
