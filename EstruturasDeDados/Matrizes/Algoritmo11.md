# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown


Algoritmo "Q11 - exMatriz"
Var
    i, j, lsupl, lsupc, lsup, n: inteiro
    m: vetor [1..5, 1..6] de inteiro
    v: vetor [1..30] de inteiro
Inicio
    lsupl <- 5
    lsupc <- 6
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 6)
            escreva("Insira o", n,"º valor do vetor: ")
            leia(v[n])
            m[i, j] <- v[n]
        fimpara
    fimpara
    lsup <- lsupl * lsupc
    escreval
    escreva("Elementos do vetor: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i],".")
        senao
            escreva(v[i],",")
        fimse
    fimpara
    escreval
    escreval("Elementos da matriz: ")
    escreval
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
