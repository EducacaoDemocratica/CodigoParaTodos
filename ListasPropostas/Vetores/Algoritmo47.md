# Exercício 47

[**Ver Análise**](Analise47.md)

```markdown
Algoritmo "Q47 - Vetor"
Var
  i, j, q, k, lsup, aux, maiorG, maiorT, primeiroT, segundoT: inteiro
  g, maisGols: vetor [1..30] de inteiro

Inicio
  lsup <- 30
  primeiroT <- 0
  segundoT <- 0

  para i de 1 ate lsup faca
    escreva("Insira o minuto do gol na", i,"ª: ")
    leia(g[i])

    enquanto ((g[i] <= 0) ou (g[i] > 90)) faca
      escreva("Insira valores de 1 a 90: ")
      leia(g[i])
    fimenquanto
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (g[i] > g[i + 1]) entao
        aux <- g[i]
        g[i] <- g[i + 1]
        g[i + 1] <- aux
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    se (g[i] < 46) entao
      primeiroT <- primeiroT + 1
    senao
      segundoT <- segundoT + 1
    fimse

    q <- 0
    para j de 1 ate lsup faca
      se (g[j] = g[i]) entao
        q <- q + 1
      fimse
    fimpara

    se (q > maiorG) entao
      maiorG <- q
      k <- 1
      maisGols[k] <- g[i]
    senao
      se ((q = maiorG) e (g[i] <> maisGols[k])) entao
        k <- k + 1
        maisGols[k] <- g[i]
      fimse
    fimse
  fimpara

  maiorT <- 0
  para i de 1 ate (lsup - 1) faca
    q <- g[i + 1] - g[i]
    se (q > maiorT) entao
      maiorT <- q
    fimse
  fimpara

  escreval
  se (k = lsup) entao
    escreval("O time marcou a mesma quantidade de gols em cada minuto registrado:", maiorG," gol(s).")
  senao
    escreva("O instante com mais gols foi/foram no(s) minuto(s)")
    para i de 1 ate k faca
      se (k <> 1) entao
        se (i = k) entao
          escreval(" e", maisGols[i], " marcando", maiorG," gols.")
        senao
          se (i = 1) entao
            escreva(maisGols[i])
          senao
            escreva(",", maisGols[i])
          fimse
        fimse
      senao
        escreval(maisGols[i], " marcando", maiorG," gols.")
      fimse
    fimpara
  fimse

  escreval("O maior intervalo sem gols foi de", maiorT," minutos.")

  se (primeiroT > segundoT) entao
    escreval("O time fez mais gols no 1º tempo, num total de", primeiroT," gols.")
  senao
    se (primeiroT < segundoT) entao
      escreval("O time fez mais gols no 2º tempo, num total de", segundoT," gols.")
    senao
      escreval("O fez a mesma quantia de gols no 1º e no 2º tempo que foi de", segundoT," gols.")
    fimse
  fimse

Fimalgoritmo
