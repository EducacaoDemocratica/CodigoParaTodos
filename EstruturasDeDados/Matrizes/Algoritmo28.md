# Exercício 28

[**Ver Análise**](Analise28.md)

Algoritmo "Q28 - exMatriz"
Var
    i, j, n, lsup: inteiro
    m: vetor [1..6, 1..6] de inteiro
Inicio
    lsup <- 4
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
            escreva(m[i, j],"")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Elementos da diagonal secundária: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) = (lsup + 1)) entao
                escreva(m[i, j],"")
            fimse
        fimpara
    fimpara
    
    escreval
Fimalgoritmo
