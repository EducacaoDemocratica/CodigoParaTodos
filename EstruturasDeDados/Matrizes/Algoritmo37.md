# Exercício 37

[**Ver Análise**](Analise37.md)

Algoritmo "Q37 - exMatriz"
Var
    i, j, p, lsup: inteiro
    m, n, o: vetor [1..4, 1..4] de inteiro
Inicio
    lsup <- 4
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * 4)
            escreva("Insira o", p, "º valor da matriz M: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * 6)
            escreva("Insira o", p, "º valor da matriz N: ")
            leia(n[i, j])
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (m[i, j] > n[i, j]) entao
                o[i, j] <- m[i, j]
            senao
                o[i, j] <- n[i, j]
            fimse
        fimpara
    fimpara
    
    escreval
    escreval("Matriz M: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz N: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(n[i, j], " ")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz O: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(o[i, j], " ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
