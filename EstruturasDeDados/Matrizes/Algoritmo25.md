# Exercício 25

[**Ver Análise**](Analise25.md)

Algoritmo "Q25 - exMatriz"
Var
    i, j, n, lsup, opcao: inteiro
    m: vetor [1..10, 1..10] de inteiro
    s: real
Inicio
    lsup <- 10
    s <- 0
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 10)
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
    escreval("Elementos acima da diagonal principal: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (i < j) entao
                escreva(m[i, j],"")
                s <- s + m[i, j]
            senao
                escreva("  ")
            fimse
        fimpara
        escreval
    fimpara
    
    escreval("Soma dos elementos:", s,".")
Fimalgoritmo
