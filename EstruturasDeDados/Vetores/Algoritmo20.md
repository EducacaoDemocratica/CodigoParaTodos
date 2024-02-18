# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown

Algoritmo "Q20 - exVetor"
Var
    i, lsup, s, c: inteiro
    m: real
    v: vetor [1..13] de inteiro
Inicio
    s <- 0
    lsup <- 13
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º valor do vetor: ")
        leia (v[i])
        enquanto (v[i] <= 0) faca
            escreva("Insira valores maiores que 0: ")
            leia (v[i])
        fimenquanto
    fimpara
    para i de 1 ate lsup faca
        se (v[i] mod 2 = 1) entao
            s <- s + v[i]
            c <- c + 1
        fimse
    fimpara
    m <- s/c
    escreval
    escreval("A média dos números ímpares do vetor é", m, ".")
Fimalgoritmo

