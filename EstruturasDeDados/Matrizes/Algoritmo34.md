# Exercício 34

[**Ver Análise**](Analise34.md)

Algoritmo "Q34 - exMatriz"
Var
    i, j, n, lsup, opcao: inteiro
    m: vetor [1..4, 1..4] de inteiro
    s: real
Inicio
    lsup <- 4
    s <- 0
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n, "º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("OPERAÇÕES COM A MATRIZ")
    escreval
    escreval("0 - Imprimir todos os elementos da matriz")
    escreval("1 - Somar os quadrados dos elementos da primeira coluna")
    escreval("2 - Somar todos os elementos da terceira linha")
    escreval("3 - Somar os elementos da diagonal principal")
    escreval("4 - Somar todos os elementos de índice par da segunda linha")
    escreval
    
    escreva("Selecione uma opção: ")
    leia(opcao)
    
    enquanto ((opcao < 0) ou (opcao > 4)) faca
        escreva("Selecione 0, 1, 2, 3 ou 4: ")
        leia(opcao)
    fimenquanto
    
    escreval
    
    se (opcao = 0) entao
        escreval("Impressão da matriz: ")
        escreval
        para i de 1 ate lsup faca
            para j de 1 ate lsup faca
                escreva(m[i, j], ",")
            fimpara
            escreval
        fimpara
    senao
        se (opcao = 1) entao
            escreval("Quadrados dos elementos da 1ª coluna:")
            escreval
            para i de 1 ate lsup faca
                escreval(m[i, 1]^2, " =", m[i, 1],"².")
                s <- s + m[i, 1]^2
            fimpara
        senao
            se (opcao = 2) entao
                escreval("Elementos da 3ª linha:")
                escreval
                para i de 1 ate lsup faca
                    se (i = lsup) entao
                        escreval(m[3, i], ".")
                    senao
                        escreva(m[3, i], ",")
                    fimse
                    s <- s + m[3, i]
                fimpara
            senao
                se (opcao = 3) entao
                    escreval("Elementos da diagonal principal:")
                    escreval
                    para i de 1 ate lsup faca
                        se (i = lsup) entao
                            escreval(m[i, i], ".")
                        senao
                            escreva(m[i, i], ",")
                        fimse
                        s <- s + m[i, i]
                    fimpara
                senao
                    escreval("Elementos de índice par da 2ª linha:")
                    escreval
                    para i de 1 ate lsup faca
                        se (i mod 2 = 0) entao
                            se (i = lsup) entao
                                escreval(m[2, i], ".")
                            senao
                                escreva(m[2, i], ",")
                            fimse
                            s <- s + m[2, i]
                        fimse
                    fimpara
                fimse
            fimse
        fimse
    fimse
    
    escreval
    escreval("Resultado da soma:", s, ".")
Fimalgoritmo
