# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown


Algoritmo "Q3 - exMatriz"
Var
    i, j, lsup, s: inteiro
    m: vetor [1..3, 1..3] de inteiro

Inicio
    lsup <- 3
    s <- 0

    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            m[i, j] <- j + ((i - 1) * 3)
            s <- s + m[i, j]
        fimpara
    fimpara

    escreval("Elementos da matriz: ")
    escreval

    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara

    escreval
    escreval("Soma dos elementos: ", s,".")

Fimalgoritmo
