# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown
Algoritmo "Q18 - Matriz"
Var
  m: vetor [1..5, 1..3] de inteiro
  v: vetor [1..5] de real
  lsupl, lsupc, i, j: inteiro
  servico: caractere

Inicio
  lsupl <- 5
  lsupc <- 3

  para i de 1 ate lsupl faca
    escreval("Dados da", i, "ª funcionária")
    escreval

    para j de 1 ate lsupc faca
      se (j = 1) entao
        servico := "mãos"
      senao
        se (j = 2) entao
          servico := "pés"
        senao
          servico := "podologia"
        fimse
      fimse

      escreva("Insira a quantidade de serviços de ", servico, ": ")
      leia(m[i, j])

      enquanto (m[i, j] < 0) faca
        escreva("A quantidade de serviços não pode ser negativa: ")
        leia(m[i, j])
      fimenquanto

      escreval
    fimpara

    escreval
  fimpara

  para i de 1 ate lsupl faca
    v[i] := m[i, 1] * 10 + m[i, 2] * 15 + m[i, 3] * 30
    escreval("Ganhos da", i, "ª funcionária: R$", v[i]:6:2, ".")
  fimpara

Fimalgoritmo
