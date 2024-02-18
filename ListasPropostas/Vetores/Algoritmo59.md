# Exercício 59

[**Ver Análise**](Analise59.md)

```markdown
Algoritmo "Q59 - Vetor"

Var
  pCarac: vetor [1..12] de caractere
  alfabeto: vetor [1..26] de caractere
  p, paux, pfuncao, pc: caractere
  i, j, k, f, c, lsup, tam, vAsc, d: inteiro

Inicio
  lsup <- 26

  para i de 1 ate lsup faca
    alfabeto[i] <- carac(64 + i)
  fimpara

  escreval("Selecione a função do programa: 0 - Crifagem; 1 - Decifragem")
  escreva("Selecione uma opção: ")
  leia(f)

  enquanto (f < 0) ou (f > 1) faca
    escreva("Selecione apenas 0 ou 1: ")
    leia(f)
  fimenquanto

  escreval
  escreva("Insira uma palavra de 6 a até 12 caracteres: ")
  leia(p)
  tam <- compr(p)

  enquanto ((tam = 0) ou (tam < 6) ou (tam > 12)) faca
    se (tam = 0) entao
      escreva("Preencha a palavra: ")
    senao
      escreva("Insira 6 a 12 caracteres: ")
    fimse
    leia(p)
    tam <- compr(p)
  fimenquanto

  p <- maiusc(p)
  k <- 0

  para i de 1 ate tam faca
    paux <- copia(p; i; 1);
    vAsc <- asc(paux)
    se ((vAsc >= 65) e (vAsc <= 90)) entao
      k <- k + 1
      pCarac[k] <- paux
    fimse
  fimpara

  escreva("Insira o valor do deslocamento: ")
  leia(d)

  enquanto ((d = 0) ou (d mod 26 = 0)) faca
    escreva("O deslocamento não pode ser 0 ou múltiplo de 26: ")
    leia(d)
  fimenquanto

  se ((d > 26) ou (d < -26)) entao
    d <- d mod 26
  fimse

  se (f = 0) entao
    pfuncao <- "cifrada"
    paux <- "decifrada"
  senao
    d <- (d * -1)
    pfuncao <- "decifrada"
    paux <- "cifrada"
  fimse

  p <- ""
  para i de 1 ate k faca
    p <- p + pCarac[i]
  fimpara

  pc <- ""
  para i de 1 ate k faca
    j <- 1
    enquanto (j <= lsup) faca
      se (pCarac[i] = alfabeto[j]) entao
        c <- j + d
        se (d > 0) entao
          se (j + d > 26) entao
            c <- (j + d) - 26
          fimse
        senao
          se (j + d <= 0) entao
            c <- (j + d) + 26
          fimse
        fimse
        pCarac[i] <- alfabeto[c]
      fimse
      j <- j + 1
    fimenquanto
    pc <- pc + pCarac[i]
  fimpara

  escreval
  escreval("Palavra ", paux," sem caracteres números ou especiais: ", p)
  escreval("Palavra ", pfuncao,": ", pc)

Fimalgoritmo
