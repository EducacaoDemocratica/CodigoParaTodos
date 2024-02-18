# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown

Algoritmo "Q19 - exVetor"
Var
    i, lsup, c: inteiro
    v: vetor [1..10] de inteiro
Inicio
    c <- 0
    lsup <- 10
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º valor do vetor: ")
        leia (v[i])
        enquanto (v[i] <= 0) faca
            escreva("Insira valores maiores que 0: ")
            leia (v[i])
        fimenquanto
    fimpara
    para i de 1 ate lsup faca
        se (v[i] mod 2 = 0) entao
            c <- c + 1
        fimse
    fimpara
    escreval
    escreval("Existem", c, " números pares do vetor.")
Fimalgoritmo

