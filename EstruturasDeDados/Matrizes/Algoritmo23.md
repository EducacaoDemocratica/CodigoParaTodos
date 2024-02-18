# Exercício 23

[**Ver Análise**](Analise23.md)

Algoritmo "Q23 - exMatriz"
Var
    i, j, n, lsup: inteiro
    m: vetor [1..7, 1..7] de inteiro
Inicio
    lsup <- 7
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 7)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("Matriz: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Elementos abaixo da diagonal principal: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (i > j) entao
                escreva(m[i, j]," ")
            senao
                escreva("  ")
            fimse
        fimpara
        escreval
    fimpara
Fimalgoritmo
