# Exercício 21

[**Ver Análise**](Analise21.md)

```markdown
Algoritmo "Q21 - Matriz"
Var
  i, j, k, lsupl, lsupc, q: inteiro
  m: vetor [1..10, 1..3] de real
  res: vetor [1..10, 1..3] de caractere
  n, es: vetor [1..10] de caractere

Inicio
  lsupl <- 5
  lsupc <- 3

  para i de 1 ate lsupl faca
    escreva("Insira o nome do", i, "º paciente: ")
    leia(n[i])
    n[i] <- maiusc(n[i])

    enquanto (n[i] = "") faca
      escreva("Preencha esse campo: ")
      leia(n[i])
    fimenquanto

    j <- 1

    enquanto (j < i) faca
      se (j <> i) entao
        enquanto (n[i] = n[j]) faca
          escreva("Esse nome já está cadastrado: ")
          leia (n[i])

          enquanto (n[i] = "") faca
            escreva("Preencha esse campo: ")
            leia(n[i])
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto
  fimenquanto

  escreva("Insira a taxa de xolesterol/Xi: ")
  leia(m[i, 1])

  enquanto ((m[i, 1] < 0) ou (m[i, 1] > 100)) faca
    escreva("A taxa deve estar entre 0 e 100: ")
    leia(m[i, 1])
  fimenquanto

  escreva("Insira a taxa de broteinas/Bi: ")
  leia(m[i, 2])

  enquanto ((m[i, 2] < -10) ou (m[i, 2] > 10)) faca
    escreva("A taxa deve estar entre -10 e 10: ")
    leia(m[i, 2])
  fimenquanto

  escreva("Insira a taxa de toroteinas/Ti: ")
  leia(m[i, 3])

  enquanto ((m[i, 3] < 50) ou (m[i, 3] > 100)) faca
    escreva("A taxa deve estar entre 50 e 100: ")
    leia(m[i, 3])
  fimenquanto

  escreval
  fimenquanto

  para i de 1 ate lsupl faca
    se ((m[i, 1] >= 30) e (m[i, 1] <= 50)) entao
      res[i, 1] <- "NORMAL"
    senao
      se (m[i, 1] < 30) entao
        res[i, 1] <- "HIPOXOLESTEROL"
      senao
        res[i, 1] <- "HIPERXOLESTEROL"
      fimse
    fimse

    se ((m[i, 2] >= 3) e (m[i, 2] <= 7)) entao
      res[i, 2] <- "NORMAL"
    senao
      se (m[i, 2] < 3) entao
        res[i, 2] <- "HIPOBROTEÍNA"
      senao
        res[i, 2] <- "HIPERBROTEÍNA"
      fimse
    fimse

    se ((m[i, 3] >= 65) e (m[i, 3] <= 80)) entao
      res[i, 3] <- "NORMAL"
    senao
      se (m[i, 3] < 65) entao
        res[i, 3] <- "HIPOTOROTEÍNA"
      senao
        res[i, 3] <- "HIPERTOROTEÍNA"
      fimse
    fimse
  fimenquanto

  para i de 1 ate lsupl faca
    q <- 0

    para j de 1 ate lsupc faca
      se (res[i, j] = "NORMAL") entao
        q <- q + 1
      fimse
    fimenquanto

    se (q = 0) entao
      es[i] <- "GRAVÍSSIMO"
    senao
      se (q = 1) entao
        es[i] <- "GRAVE"
      senao
        se (q = 2) entao
          es[i] <- "MODERADO"
        senao
          es[i] <- "SAUDÁVEL"
        fimse
      fimse
    fimse
  fimenquanto

  fimenquanto

  para i de 1 ate lsupl faca
    escreval("Paciente: ", n[i], ".")
    escreval("Xolesterol:", m[i, 1], " = ", res[i, 1], ".")
    escreval("Broteínas:", m[i, 2], " = ", res[i, 2], ".")
    escreval("Toroteínas:", m[i, 3], " = ", res[i, 3], ".")
    escreval("Estado de saúde: ", es[i], ".")
    escreval
  fimenquanto
Fimalgoritmo
