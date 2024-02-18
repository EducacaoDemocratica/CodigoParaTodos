# Exercício 50

[**Ver Análise**](Analise50.md)

```markdown
Algoritmo "Q50 - Vetor"
Var
  i, lsup, n, c, f: inteiro
  v: vetor [1..30] de inteiro

Inicio
  lsup <- 30
  n <- 0
  c <- 0
  f <- 1

  enquanto (f <> 0) faca
    escreval("0 - Sair; 1 - Estacionar veículo; 2 - Liberar vaga")
    escreva("Selecione uma função: ")
    leia (f)

    enquanto ((f < 0) ou (f > 2)) faca
      escreva("Função não encontrada. Insira outra: ")
      leia (f)
    fimenquanto

    escreval

    se ((f = 1) e (c = lsup)) entao
      escreval("Todas as vagas foram preenchidas. Por favor, libere uma vaga.")
      escreval
    senao
      se ((f = 2) e (c = 0)) entao
        escreval("Todas as vagas estão vazias. Por favor, preencha uma vaga.")
        escreval
      senao
        se (f <> 0) entao
          escreval("Listagem das vagas: ")
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

          enquanto ((n <= 0) ou (n > 30)) faca
            escreva("Essa vaga não existe. Escolha outra: ")
            leia(n)
          fimenquanto

          se (f = 1) entao
            se (v[n] = 1) entao
              escreval("Essa vaga já foi ocupada.")
            senao
              escreval("Vaga", n," ocupada com sucesso.")
              v[n] <- 1
              c <- c + 1
            fimse
          senao
            se (v[n] = 0) entao
              escreval("Não existe um carro nessa vaga.")
            senao
              escreval("Vaga", n," liberada com sucesso.")
              v[n] <- 0
              c <- c - 1
            fimse
          fimse
          escreval
        fimse
      fimse
    fimse
  fimenquanto

  escreval
  escreval("Sistema encerrado com sucesso.")
Fimalgoritmo
