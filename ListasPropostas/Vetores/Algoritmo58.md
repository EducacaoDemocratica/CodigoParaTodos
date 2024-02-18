# Exercício 58

[**Ver Análise**](Analise58.md)

```markdown
Algoritmo "Q58 - Vetor"

Var
  pCarac: vetor [1..15] de caractere
  cifra: vetor [1..10] de caractere
  p, paux, pfuncao, pc: caractere
  i, j, k, f, lsup, tam, vAsc: inteiro

Inicio
  lsup <- 10
  cifra[1] <- "J"
  cifra[2] <- "U"
  cifra[3] <- "L"
  cifra[4] <- "I"
  cifra[5] <- "O"
  cifra[6] <- "C"
  cifra[7] <- "E"
  cifra[8] <- "S"
  cifra[9] <- "A"
  cifra[10] <- "R"

  escreval("Selecione a função do programa: 0 - Crifagem; 1 - Decifragem")
  escreva("Selecione uma opção: ")
  leia(f)

  enquanto (f < 0) ou (f > 1) faca
    escreva("Selecione apenas 0 ou 1: ")
    leia(f)
  fimenquanto

  escreval
  escreva("Insira uma palavra de 6 até 15 caracteres: ")
  leia(p)
  tam <- compr(p)

  enquanto ((tam = 0) ou (tam < 6) ou (tam > 15)) faca
    se (tam = 0) entao
      escreva("Preencha a palavra: ")
    senao
      escreva("Insira 6 a 15 caracteres: ")
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

  p <- ""
  para i de 1 ate k faca
    p <- p + pCarac[i]
  fimpara

  pc <- ""
  para i de 1 ate k faca
    j <- 1
    enquanto (j <= lsup) faca
      se (pCarac[i] = cifra[j]) entao
        se (j > 5) entao
          pCarac[i] <- cifra[j - 5]
        senao
          pCarac[i] <- cifra[j + 5]
        fimse
      j <- lsup
      fimse
      j <- j + 1
    fimenquanto
    pc <- pc + pCarac[i]
  fimpara

  se (f = 0) entao
    pfuncao <- "cifrada"
    paux <- "decifrada"
  senao
    pfuncao <- "decifrada"
    paux <- "cifrada"
  fimse

  escreval
  escreval("Palavra ", paux," sem caracteres números ou especiais: ", p)
  escreval("Palavra ", pfuncao,": ", pc)

Fimalgoritmo
