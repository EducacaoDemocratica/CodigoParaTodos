# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown
Algoritmo "Q14 - Matriz"
Var
  m: vetor [1..3, 1..3] de inteiro
  vaux: vetor [1..9] de inteiro
  sc, sl: vetor [1..3] de inteiro
  i, j, k, p, lsup, sp, ss: inteiro
  magico: logico

Inicio
  lsup <- 3
  magico <- verdadeiro

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      p <- j + ((i - 1) * lsup)
      escreva("Insira o", p, "º valor da matriz: ")
      leia(m[i, j])
      vaux[p] <- m[i, j]

      k <- 1
      enquanto (k < p) faca
        se (k <> p) entao
          enquanto (vaux[k] = m[i, j]) faca
            escreva("Esse valor já está na matriz: ")
            leia(m[i, j])
            vaux[p] <- m[i, j]
          fimenquanto
        fimse
        k <- k + 1
      fimenquanto
    fimpara
  fimpara

  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      sc[i] <- sc[i] + m[j, i]
      sl[i] <- sl[i] + m[i, j]
      se (i = j) entao
        sp <- sp + m[i, j]
      fimse
      se ((i + j) = (lsup + 1)) entao
        ss <- ss + m[i, j]
      fimse
    fimpara
  fimpara

  se (ss <> sp) entao
    magico <- falso
  fimse

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      se (sc[i] <> sl[j]) entao
        magico <- falso
      fimse
    fimpara
  fimpara

  escreval

  escreval("Matriz:")
  escreval

  para i de 1 ate lsup faca
    para j de 1 ate lsup faca
      escreva(m[i, j])
    fimpara
    escreval
  fimpara

  escreval

  se (magico = verdadeiro) entao
    escreval("A matriz é um quadrado mágico e a soma das linhas, colunas e diagonais é", ss, ".")
  senao
    escreval("A matriz não é um quadrado mágico.")
  fimse

Fimalgoritmo
