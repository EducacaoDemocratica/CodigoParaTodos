# Exercício 22

[**Ver Análise**](Analise22.md)

Algoritmo "Q22 - exMatriz"
Var
    i, j, n, lsup: inteiro
    m: vetor [1..6, 1..6] de inteiro
Inicio
    lsup <- 6
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 6)
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
    escreval("Elementos da diagonal principal: ")
    escreval
    
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(m[i, i],".")
        senao
            escreva(m[i, i],",")
        fimse
    fimpara
Fimalgoritmo
