# Exercício 39

[**Ver Análise**](Analise39.md)

Algoritmo "Q39 - exMatriz"
Var
    i, j, n, lsup: inteiro
    m, mti: vetor [1..4, 1..4] de real
Inicio
    lsup <- 4
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            enquanto ((m[i, j] < 1) ou (m[i, j] > 20)) faca
                escreva("Insira um valor do intervalo [1, 20]: ")
                leia(m[i, j])
            fimenquanto
        fimpara
    fimpara
    
    escreval
    escreval("Matriz original: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (i < j) entao
                mti[i, j] <- 0
            senao
                mti[i, j] <- m[i, j]
            fimse
        fimpara
    fimpara
    
    escreval
    escreval("Matriz triangular inferior: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(mti[i, j], " ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
