# Exercício 29

[**Ver Análise**](Analise29.md)

```markdown
Algoritmo "Q29 - Vetor"
Var
  i, iMaisVendido, iMaiorRetorno, lsup: inteiro
  q: vetor [1..9] de inteiro
  t, maiorRetorno, maisVendido, d: real
  p: vetor [1..9] de real

Inicio
  lsup <- 9
  t <- 0

  para i de 1 ate lsup faca
    escreva("Insira o preço do", i, "º produto: ")
    leia(p[i])

    enquanto (p[i] <= 0) faca
      escreva("O preço deve ser maior que 0: ")
      leia(p[i])
    fimenquanto

    escreva("Insira a quantidade vendida do", i, "º produto: ")
    leia(q[i])

    enquanto (q[i] < 0) faca
      escreva("A quantidade vendida não pode ser negativa: ")
      leia(q[i])
    fimenquanto

    escreval
  fimpara

  para i de 1 ate lsup faca
    se (i = 1) entao
      maisVendido <- q[i]
      iMaisVendido <- i
      maiorRetorno <- (q[i] * p[i])
      iMaiorRetorno <- i
    senao
      se (q[i] > maisVendido) entao
        maisVendido <- q[i]
        iMaisVendido <- i
      fimse

      se ((q[i] * p[i]) > maiorRetorno) entao
        maiorRetorno <- (q[i] * p[i])
        iMaiorRetorno <- i
      fimse
    fimse

    t <- t + (q[i] * p[i])
  fimpara

  escreval("Total vendido: R$", t)
  escreval("O produto que deu maior retorno foi o", iMaiorRetorno, "º com R$", maiorRetorno)

  se (iMaisVendido = iMaiorRetorno) entao
    escreval("O produto mais vendido é o mesmo de maior retorno financeiro.")
  senao
    maisVendido <- q[iMaisVendido] * p[iMaisVendido]
    escreval("O produto mais vendido arrecadou: R$", maisVendido:6:2)
    d <- maiorRetorno - maisVendido
    escreval("A diferença na arrecadação entre o produto de retorno e o mais vendido é R$", d:6:2, ".")
  fimse

Fimalgoritmo
