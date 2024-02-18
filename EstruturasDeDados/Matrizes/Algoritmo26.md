# Exercício 26

[**Ver Análise**](Analise26.md)

Algoritmo "Q26 - exMatriz"
Var
    i, j, n, lsup, opcao: inteiro
    m: vetor [1..9, 1..9] de inteiro
    p: real
Inicio
    lsup <- 9
    p <- 1
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 9)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("Matriz: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j],"")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Elementos abaixo da diagonal principal: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (i > j) entao
                escreva(m[i, j],"")
                p <- p * m[i, j]
            senao
                escreva("  ")
            fimse
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Produto dos elementos:", p,".")
Fimalgoritmo
