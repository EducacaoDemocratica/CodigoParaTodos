# Exercício 49

[**Ver Análise**](Analise49.md)

```markdown
Algoritmo "Q49 - Vetor"
Var
  i, lsup, n, c: inteiro
  v: vetor [1..30] de inteiro

Inicio
  lsup <- 30
  n <- 0
  c <- 0

  enquanto (n <> -1) faca
    se (c <> lsup) entao
      escreval("(Insira -1 para finalizar o programa.)")
      escreval("Selecione uma vaga para estacionar um veículo: ")
      escreval
      para i de 1 ate lsup faca
        se (v[i] = 0) entao
          escreval("Vaga", i,": DISPONÍVEL")
        senao
          escreval("Vaga", i,": OCUPADA")
        fimse
      fimpara
      escreval
      escreva("Escolha uma vaga: ")
      leia(n)

      enquanto ( ((n <= 0) ou (n > 30)) e (n <> -1)) faca
        escreva("Essa vaga não existe. Escolha outra: ")
        leia(n)
      fimenquanto

      se (n <> -1) entao
        se (v[n] = 1) entao
          escreval("Essa vaga já foi ocupada.")
        senao
          escreval("Vaga", n," ocupada com sucesso.")
          v[n] <- 1
          c <- c + 1
        fimse
      fimse

      escreval
    senao
      escreval("Não existem vagas disponíveis.")
      n <- -1
    fimse
  fimenquanto

  escreval
  escreval("Sistema encerrado com sucesso.")
Fimalgoritmo
