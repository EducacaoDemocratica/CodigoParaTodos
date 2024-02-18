# Exercício 30

[**Ver Análise**](Analise30.md)

Algoritmo "Q30 - exMatriz"
Var
    i, j, n, lsup, menor: inteiro
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
    
    n <- 0
    escreval
    escreval("Elementos acima da diagonal secundária: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) < (lsup + 1)) entao
                escreva(m[i, j],"")
                se (m[i, j] mod 2 = 0) entao
                    n <- n + 1
                    se (n = 1) entao
                        menor <- m[i, j]
                    senao
                        se (m[i, j] < menor) entao
                            menor <- m[i, j]
                        fimse
                    fimse
                fimse
            fimse
        fimpara
        escreval
    fimpara
    
    escreval("O menor valor par acima da diagonal secundária:", menor, ".")
Fimalgoritmo
