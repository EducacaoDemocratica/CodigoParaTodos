# Exercício 38

[**Ver Análise**](Analise38.md)

Algoritmo "Q38 - exMatriz"
Var
    i, j, lsup: inteiro
    m: vetor [1..10, 1..10] de real
Inicio
    lsup <- 10
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (i < j) entao
                m[i, j] <- (2 * i) + (7 * j) - 2
            senao
                se (i = j) entao
                    m[i, j] <- (3 * (i^2)) - 1
                senao
                    m[i, j] <- (4 * (i^3)) - (5 * (j^2)) + 1
                fimse
            fimse
        fimpara
    fimpara
    
    escreval
    escreval("Matriz gerada: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
