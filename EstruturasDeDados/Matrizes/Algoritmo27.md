# Exercício 27

[**Ver Análise**](Analise27.md)

Algoritmo "Q27 - exMatriz"
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
            escreva(m[i, j],"")
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Elementos da diagonal principal e abaixo dela: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (i >= j) entao
                se ((i = 1) e (j = 1)) entao
                    maior <- m[i, j]
                senao
                    se (m[i, j] > maior) entao
                        maior <- m[i, j]
                    fimse
                fimse
                escreva(m[i, j],"")
            senao
                escreva("  ")
            fimse
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("O maior elemento na diagonal principal ou abaixo dela é", maior,".")
Fimalgoritmo
