# Exercício 24

[**Ver Análise**](Analise24.md)

Algoritmo "Q24 - exMatriz"
Var
    i, j, n, lsup: inteiro
    m: vetor [1..9, 1..9] de inteiro
Inicio
    lsup <- 9
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
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Elementos ímpares acima da diagonal principal: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i < j) e (m[i, j] mod 2 = 1)) entao
                escreva(m[i, j]," ")
            senao
                escreva("  ")
            fimse
        fimpara
        escreval
    fimpara
Fimalgoritmo
