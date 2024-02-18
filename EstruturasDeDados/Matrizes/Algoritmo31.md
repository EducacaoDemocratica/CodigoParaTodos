# Exercício 31

[**Ver Análise**](Analise31.md)

Algoritmo "Q31 - exMatriz"
Var
    i, j, n, lsup, maior: inteiro
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
            escreva(m[i, j],"")
        fimpara
        escreval
    fimpara
    
    n <- 0
    escreval
    escreval("Elementos da diagonal secundária e acima dela: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) <= (lsup + 1)) entao
                escreva(m[i, j],"")
                n <- n + 1
                se (n = 1) entao
                    maior <- m[i, j]
                senao
                    se (m[i, j] > maior) entao
                        maior <- m[i, j]
                    fimse
                fimse
            fimse
        fimpara
    fimpara
    
    escreval
    fimpara
    
    escreval("O maior valor acima ou na diagonal secundária:", maior, ".")
Fimalgoritmo
