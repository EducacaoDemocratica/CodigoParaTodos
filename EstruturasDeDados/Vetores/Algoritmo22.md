# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown

Algoritmo "Q22 - exVetor"
Var
    i, lsup, s: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    para i de 1 ate lsup faca
        escreva("Insira o ", i, "º número: ")
        leia(v[i])
        enquanto (v[i] <= 0) faca
            escreva("Insira um número maior que 0: ")
            leia(v[i])
        fimenquanto
    fimpara
    escreval
    para i de 1 ate lsup faca
        s <- s + v[i]
    fimpara
    escreval("Média dos valores inseridos: ", s / i)
Fimalgoritmo