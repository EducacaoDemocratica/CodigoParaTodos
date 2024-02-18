# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown
Algoritmo "Q12 - Vetor"
Var
  n, i, lsup: inteiro
  v: vetor [1..10] de inteiro
  presente: logico

Inicio
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
    fimse
  fimpara

  se (presente = verdadeiro) entao
    escreval(n, " está presente na estrutura.")
  senao
    escreval(n, " não está presente na estrutura.")
  fimse

Fimalgoritmo
