# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown
Algoritmo "Q17 - Matriz"
Var
  m: vetor [1..50, 1..2] de inteiro
  n: vetor [1..50] de caractere
  lsup, i, j: inteiro
  abaixo: logico

Inicio
  lsup <- 50
  abaixo <- falso

  para i de 1 ate lsup faca
    escreva("Insira o nome da", i, "ª planta: ")
    leia(n[i])
    n[i] <- maiusc(n[i])
    j <- 1

    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (n[i] = n[j]) faca
          escreva("Esse nome já está cadastrado: ")
          leia (n[i])
          n[i] <- maiusc(n[i])
          j <- 1
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto

    escreva("Insira a quantidade em estoque: ")
    leia(m[i, 1])

    enquanto (m[i, 1] < 0) faca
      escreva("A quantidade não deve ser negativa: ")
      leia(m[i, 1])
    fimenquanto

    escreva("Insira o estoque ideal: ")
    leia(m[i, 2])

    enquanto (m[i, 2] <= 0) faca
      escreva("A quantidade deve ser maior que 0: ")
      leia(m[i, 2])
    fimenquanto

    se (m[i, 1] < m[i, 2]) entao
      abaixo <- verdadeiro
    fimse

    escreval
  fimpara

  escreval

  se (abaixo = falso) entao
    escreval("Não existem plantas abaixo do estoque.")
  senao
    escreval("Plantas abaixo do estoque e quantidade necessária para reposição: ")
    escreval
    para i de 1 ate lsup faca
      se (m[i, 1] < m[i, 2]) entao
        escreval(n[i], ": é necessário comprar mais", m[i, 2] - m[i, 1], " unidades.")
      fimse
    fimpara
  fimse

Fimalgoritmo
