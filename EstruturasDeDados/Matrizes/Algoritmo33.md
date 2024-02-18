# Exercício 33

[**Ver Análise**](Analise33.md)

Algoritmo "Q33 - exMatriz"
Var
    i, j, n, lsup, maior: inteiro
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
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    n <- 0
    escreval
    escreval("Matriz sem as diagonais principal e secundária: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (((i + j) <> (lsup + 1)) e (i <> j)) entao
                escreva(m[i, j], " ")
            fimse
        fimpara
    fimpara
    
    escreval
    fimpara
Fimalgoritmo
