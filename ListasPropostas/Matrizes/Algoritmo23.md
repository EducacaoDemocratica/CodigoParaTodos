# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown
Algoritmo "Q23 - Matriz"
Var
  m: vetor [1..10, 1..10] de real
  v: vetor [1..10] de inteiro
  id: vetor [1..10] de caractere
  i, j, lsup, maior: inteiro
  num: caractere
  s, aux, media: real

Inicio
  lsup <- 10
  media <- 0

  para i de 1 ate lsup faca
    escreval("Dados do", i," aluno: ")
    escreval
    escreva("Matrícula: ")
    leia(v[i])

    enquanto ((v[i] <= 0) ou (v[i] > 10000)) faca
      escreva("Insira dados válidos: ")
      leia(v[i])
    fimenquanto

    j <- 0

    enquanto (j < (i - 1)) faca
      j <- j + 1

      enquanto (v[i] = v[j]) faca
        escreva("Entrada duplicada. Insira outro valor: ")
        leia(v[i])
      fimenquanto

      j <- 1

      enquanto ((v[i] <= 0) ou (v[i] > 10000)) faca
        escreva("Insira dados válidos: ")
        leia(v[i])
      fimenquanto
    fimenquanto
    fimenquanto

    num <- numpcarac(v[i])

    se (v[i] < 10) entao
      id[i] <- "000" + num
    senao
      se (v[i] < 100) entao
        id[i] <- "00" + num
      senao
        se (v[i] < 1000) entao
          id[i] <- "0" + num
        senao
          id[i] <- num
        fimse
      fimse
    fimse

    s <- 0

    escreval

    para j de 1 ate 5 faca
      escreva("Insira a nota da", j,"º prova: ")
      leia(m[i, j])

      enquanto ((m[i, j] < 0) ou (m[i, j] > 12)) faca
        escreva("A nota da prova deve estar entre 0 e 12: ")
        leia(m[i, j])
      fimenquanto

      s <- s + m[i, j]
    fimpara

    m[i, 10] <- s/j
    s <- 0

    escreval

    para j de 6 ate 9 faca
      escreva("Insira a nota do", (j - 5),"º trabalho: ")
      leia(m[i, j])

      enquanto ((m[i, j] < 0) ou (m[i, j] > 10)) faca
        escreva("A nota do trabalho deve estar entre 0 e 10: ")
        leia(m[i, j])
      fimenquanto

      s <- s + m[i, j]
    fimpara

    m[i, 10] <- m[i, 10] + s/4
    media <- media + m[i, 10]

    se (i = 1) entao
      maior <- i
      aux <- m[i, 10]
    senao
      se (m[i, 10] > aux) entao
        maior <- i
        aux <- m[i, 10]
      fimse
    fimse

    escreval
  fimenquanto

  media <- media/i

  para i de 1 ate lsup faca
    escreval(i,"º aluno: ", id[i],"; Final =", m[i, 10],".")
  fimpara

  escreval
  escreval("Média das notas finais:", media,".")
  escreval("Aluno com a maior nota final: Matrícula = ", id[maior],"; Final =", m[maior, 10],".")
Fimalgoritmo
