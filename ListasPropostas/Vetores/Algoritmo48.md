# Exercício 48

[**Ver Análise**](Analise48.md)

```markdown
Algoritmo "Q48 - Vetor"
Var
  i, j, k, lsup, lsupAux, aux, achou: inteiro
  n: vetor [1..80] de inteiro
  naux, fa: vetor [1..11] de inteiro
  fr: vetor [1..11] de real

Inicio
  lsup <- 80
  lsupAux <- 11

  para i de 1 ate lsup faca
    escreva("Insira a",i,"ª nota: ")
    leia (n[i])

    enquanto ((n[i] < 0) ou (n[i] > 10)) faca
      escreva("A nota deve estar entre 0 e 10: ")
      leia (n[i])
    fimenquanto
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (n[i] > n[i + 1]) entao
        aux <- n[i]
        n[i] <- n[i + 1]
        n[i + 1] <- aux
      fimse
    fimpara
  fimpara

  escreval

  k <- 0
  para i de 1 ate lsup faca
    achou <- 1
    se(n[i] = 0) entao
      k <- 1
      fa[k] <- fa[k] + 1
    senao
      para j de 1 ate lsupAux faca
        se (naux[j] = n[i]) entao
          fa[j] <- fa[j] + 1
          achou <- 0
        fimse
      fimpara

      se (achou = 1) entao
        k <- k + 1
        naux[k] <- n[i]
        fa[k] <- 1
      fimse
    fimse
  fimpara

  para i de 1 ate k faca
    fr[i] <- ((fa[i]/lsup) * 100)
  fimpara

  escreval("Notas e suas frequências absolutas e relativas das", lsup," notas inseridas:")
  escreval

  para i de 1 ate k faca
    escreval("Nota:",naux[i]," / FA:", fa[i], " / FR:", fr[i],"%")
  fimpara

Fimalgoritmo
