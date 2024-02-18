# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown
Algoritmo "Q22 - Matriz"
Var
  m: vetor [1..10, 1..4] de inteiro
  id: vetor [1..10] de caractere
  num: caractere
  i, lsup, maior, s, aux: inteiro

Inicio
  lsup <- 10

  para i de 1 ate lsup faca
    escreval("Dados do", i, " aluno: ")
    escreval

    escreva("Matrícula: ")
    leia(m[i, 1])

    enquanto ((m[i, 1] <= 0) ou (m[i, 1] > 10000)) faca
      escreva("Insira dados válidos: ")
      leia(m[i, 1])
    fimenquanto

    s <- 0

    enquanto (s < (i - 1)) faca
      s <- s + 1

      enquanto (m[i, 1] = m[s, 1]) faca
        escreva("Entrada duplicada. Insira outro valor: ")
        leia(m[i, 1])
      fimenquanto

      s <- 1

      enquanto ((m[i, 1] <= 0) ou (m[i, 1] >= 10000)) faca
        escreva("Insira dados válidos: ")
        leia(m[i, 1])
      fimenquanto
    fimenquanto
    fimenquanto

    num <- numpcarac(m[i, 1])

    se (m[i, 1] < 10) entao
      id[i] <- "000" + num
    senao
      se (m[i, 1] < 100) entao
        id[i] <- "00" + num
      senao
        se (m[i, 1] < 1000) entao
          id[i] <- "0" + num
        senao
          id[i] <- num
        fimse
      fimse
    fimse

    escreva("Sexo(1 - Masculino; 2 - Feminino): ")
    leia(m[i, 2])

    enquanto (m[i, 2] <> 1) e (m[i, 2] <> 2) faca
      escreva("Insira dados válidos: ")
      leia(m[i, 2])
    fimenquanto

    id[i] <- id[i] + numpcarac(m[i, 2])

    escreva("Código de curso: ")
    leia(m[i, 3])

    enquanto ((m[i, 3] <= 0) ou (m[i, 3] >= 1000)) faca
      escreva("Insira dados válidos: ")
      leia(m[i, 3])
    fimenquanto

    num <- numpcarac(m[i, 3])

    se (m[i, 3] < 10) entao
      id[i] <- id[i] + "00" + num
    senao
      se (m[i, 3] < 100) entao
        id[i] <- id[i] + "0" + num
      senao
        id[i] <- id[i] + num
      fimse
    fimse

    escreva("Insira o Coeficiente de Rendimento: ")
    leia(m[i, 4])

    enquanto ((m[i, 4] < 0) ou (m[i, 4] >= 100)) faca
      escreva("Insira dados válidos: ")
      leia(m[i, 4])
    fimenquanto

    s <- 0

    enquanto (s < (i - 1)) faca
      s <- s + 1

      enquanto (m[i, 4] = m[s, 4]) faca
        escreva("Entrada duplicada. Insira outro valor: ")
        leia(m[i, 4])

        enquanto ((m[i, 4] < 0) ou (m[i, 4] >= 100)) faca
          escreva("Insira dados válidos: ")
          leia(m[i, 4])
        fimenquanto
      fimenquanto

      s <- 1
    fimenquanto
    fimenquanto

    num <- numpcarac(m[i, 4])

    se (m[i, 4] < 10) entao
      id[i] <- id[i] + "0" + num
    senao
      id[i] <- id[i] + num
    fimse

    se (m[i, 2] = 1) entao
      se (i = 1) entao
        maior <- i
        aux <- m[i, 4]
      fimse

      se (m[i, 4] > aux) entao
        maior <- i
        aux <- m[i, 4]
      fimse
    fimse

    escreval
  fimenquanto

  se (aux = 0) entao
    escreval("Nenhum dado de algum aluno foi inserido.")
  senao
    escreval("O aluno ", id[maior], " possui o maior Coeficiente de Rendimento.")
    escreval("CR =", m[maior, 4], ".")
  fimse
Fimalgoritmo
