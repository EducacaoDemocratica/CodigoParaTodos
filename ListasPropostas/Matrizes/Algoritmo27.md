# Exercício 27

[**Ver Análise**](Analise27.md)

```markdown
Algoritmo "Q27 - Matriz"
Var
  alfa: vetor [1..26, 1..26] de caractere
  p, c: vetor [1..15] de caractere
  palavra, chave, paux, resultado: caractere
  li, cl, d, ch: vetor [1..15] de inteiro
  i, j, k, lsup, vAsc, f, tam, tamP, tamC: inteiro

Inicio
  lsup <- 26
  k <- 1
  tamP <- 0
  tamC <- 0

  para i de 1 ate 26 faca
    para j de 1 ate 26 faca
      alfa[i, j] <- (carac(64+k))
      k <- k + 1
      se (k > 26) entao
        k <- k mod 26
      fimse
    fimpara
    k <- k + 1
  fimpara

  escreval("0 - Criptografar. 1 - Descriptografar.")
  escreval
  escreva("Entre com a função da cifra: ")
  leia(f)

  enquanto ((f > 1) ou (f < 0)) faca
    escreva("Entre com 0 ou 1: ")
    leia(f)
  fimenquanto

  escreval
  escreva("Insira a palavra: ")
  leia(palavra)
  tam <- compr(palavra)

  enquanto ((tam = 0) ou (tam > 15)) faca
    se (tam = 0) entao
      escreva("Preencha a palavra: ")
    senao
      escreva("Insira até 15 caracteres: ")
    fimse
    leia(palavra)
    tam <- compr(palavra)
  fimenquanto

  palavra <- maiusc(palavra)

  para i de 1 ate tam faca
    paux <- copia(palavra, i, 1)
    vAsc <- asc(paux)

    se ((vAsc >= 65) e (vAsc <= 90)) entao
      tamP <- tamP + 1
      p[tamP] <- paux
    fimse
  fimpara

  palavra <- ""

  para i de 1 ate tamP faca
    palavra <- palavra + p[i]

    para k de 1 ate lsup faca
      se (alfa[1, k] = p[i]) entao
        cl[i] <- k
      fimse
    fimpara
  fimpara

  escreva("Insira a chave de criptografia: ")
  leia(chave)
  tam <- compr(chave)

  enquanto ((tam = 0) ou (tam > 15)) faca
    se (tam = 0) entao
      escreva("Preencha a palavra: ")
    senao
      escreva("Insira até 15 caracteres: ")
    fimse
    leia(chave)
    tam <- compr(chave)
  fimenquanto

  chave <- maiusc(chave)

  para i de 1 ate tam faca
    paux <- copia(chave, i, 1)
    vAsc <- asc(paux)

    se ((vAsc >= 65) e (vAsc <= 90)) entao
      tamC <- tamC + 1
      c[tamC] <- paux
    fimse
  fimpara

  chave <- ""

  para i de 1 ate tamC faca
    chave <- chave + c[i]

    para k de 1 ate lsup faca
      se (alfa[k, 1] = c[i]) entao
        ch[i] <- k
      fimse
    fimpara
  fimpara

  escreval
  k <- 0

  enquanto (tamC < tamP) faca
    tamC <- tamC + 1
    k <- k + 1
    c[tamC] <- c[k]
  fimenquanto

  para i de 1 ate tamC faca
    para k de 1 ate lsup faca
      se (alfa[k, 1] = c[i]) entao
        li[i] <- k
      fimse
    fimpara
  fimpara

  resultado <- ""

  se (f = 0) entao
    paux <- "criptografada"

    para i de 1 ate tamP faca
      resultado <- resultado + alfa[li[i], cl[i]]
    fimpara
  senao
    paux <- "descriptografada"

    para i de 1 ate tamP faca
      para k de 1 ate lsup faca
        se (p[i] = alfa[li[i], k]) entao
          d[i] <- k
        fimse
      fimpara
    fimpara

    para i de 1 ate tamP faca
      resultado <- resultado + alfa[1, d[i]]
    fimpara
  fimse

  escreval
  escreval("Palavra escolhida: ", palavra, ".")
  escreval("Chave: ", chave, ".")
  escreval("Palavra ", paux, ": ", resultado, ".")

Fimalgoritmo
