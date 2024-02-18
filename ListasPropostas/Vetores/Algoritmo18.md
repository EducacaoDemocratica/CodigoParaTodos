# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown
Algoritmo "Q18 - Vetor"
Var
  i, j, lsup, ni, np, aux: inteiro
  v, par, imp: vetor [1..20] de inteiro

Inicio
  ni <- 0
  np <- 0

  escreva("Insira um número: ")
  leia(lsup)

  enquanto ((lsup <= 0) ou (lsup > 20)) faca
    escreva("Insira um número maior que 0 e menor/igual a 20: ")
    leia(lsup)
  fimenquanto

  escreval

  para i de 1 ate lsup faca
    escreva("Insira o", i, "º número do vetor: ")
    leia(v[i])
  fimpara

  escreval

  escreva("Vetor antes da ordenação:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  para i de 1 ate lsup faca
    se (v[i] mod 2 = 0) entao
      np <- np + 1
      par[np] <- v[i]
    senao
      ni <- ni + 1
      imp[ni] <- v[i]
    fimse
  fimpara

  para j de (np - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (par[i] > par[i + 1]) entao
        aux <- par[i]
        par[i] <- par[i + 1]
        par[i + 1] <- aux
      fimse
    fimpara
  fimpara

  para j de (ni - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (imp[i] < imp[i + 1]) entao
        aux <- imp[i]
        imp[i] <- imp[i + 1]
        imp[i + 1] <- aux
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    se (i <= np) entao
      v[i] <- par[i]
    senao
      v[i] <- imp[i - np]
    fimse
  fimpara

  escreva("Vetor depois da ordenação:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

Fimalgoritmo
