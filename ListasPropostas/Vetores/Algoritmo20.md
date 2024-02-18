# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown
Algoritmo "Q20 - Vetor"
Var
  i, j, k, n, lsup, aux, achou: inteiro
  presente, existe: logico
  v: vetor [1..80] de inteiro

Inicio
  lsup <- 80
  existe <- verdadeiro

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º valor do vetor: ")
    leia (v[i])
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (v[i] > v[i + 1]) entao
        aux <- v[i]
        v[i] <- v[i + 1]
        v[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval
  escreva("Insira o número que você deseja procurar: ")
  leia (n)
  i <- 1

  enquanto ((i < lsup) e existe = verdadeiro) faca
    se (v[i] > n) entao
      existe <- falso
    senao
      se (v[i] = n) entao
        presente <- verdadeiro
      fimse
    fimse
    i <- i + 1
  fimenquanto

  escreval

  se (presente = verdadeiro) entao
    escreval(n, " está presente na estrutura.")
  senao
    escreval(n, " não está presente na estrutura.")
  fimse

Fimalgoritmo
