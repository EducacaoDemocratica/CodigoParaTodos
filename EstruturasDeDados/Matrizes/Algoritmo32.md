# Exercício 32

[**Ver Análise**](Analise32.md)

Algoritmo "Q32 - exMatriz"
Var
    i, j, n, lsup, opcao: inteiro
    m: vetor [1..10, 1..10] de inteiro
Inicio
    lsup <- 10
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
            escreva(m[i, j], ",")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz sem a diagonal secundária: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) <> (lsup + 1)) entao
                escreva(m[i, j], " ")
            fimse
        fimpara
    fimpara
    
    escreval
    fimpara
Fimalgoritmo
