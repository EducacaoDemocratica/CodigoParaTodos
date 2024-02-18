# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown
Algoritmo "Q16 - Vetor"
Var
  i, j, k, lsup, aux: inteiro
  v: vetor [1..20] de inteiro

Inicio
  escreva("Insira um número: ")
  leia(lsup)

  enquanto ((lsup <= 0) ou (lsup > 20)) faca
    escreva("Insira um número maior que 0 e menor/igual a 20: ")
    leia(lsup)
  fimenquanto

  escreval

  para i de 1 ate lsup faca
    escreva("Insira o", i,"º número do vetor: ")
    leia(v[i])
  fimpara

  escreval

  escreva("Insira um número k: ")
  leia(k)

  enquanto ((k <= 0) ou (k > lsup)) faca
    escreva("Insira um número maior que 0 e menor/igual a", lsup, ": ")
    leia(k)
  fimenquanto

  escreval

  escreva("Vetor antes da ordenação:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  escreval(k, "º termo antes da ordenação:", v[k], ".")

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

  escreva("Vetor após a ordenação:")
  para i de 1 ate lsup faca
    se (i = lsup) entao
      escreval(v[i], ".")
    senao
      escreva(v[i], ",")
    fimse
  fimpara

  escreval(k, "º termo após da ordenação:", v[k], ".")

Fimalgoritmo
