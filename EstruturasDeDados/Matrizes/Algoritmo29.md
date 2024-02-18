# Exercício 29

[**Ver Análise**](Analise29.md)

Algoritmo "Q29 - exMatriz"
Var
    i, j, n, k, aux, lsup, lsupaux, achou, maior, vezes: inteiro
    m: vetor [1..5, 1..5] de inteiro
    v, vaux, r: vetor[1..10] de inteiro
Inicio
    lsup <- 5
    lsupaux <- 10
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 5)
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
    escreval("Elementos abaixo da diagonal secundária: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) > (lsup + 1)) entao
                escreva(m[i, j],"")
                n <- n + 1
                v[n] <- m[i, j]
            fimse
        fimpara
        escreval
    fimpara
    
    para j de (lsupaux - 1) ate 1 passo -1 faca
        para i de 1 ate j faca
            se (v[i] > v[i + 1]) entao
                aux <- v[i]
                v[i] <- v[i + 1]
                v[i + 1] <- aux
            fimse
        fimpara
    fimpara
    
    k <- 0
    para i de 1 ate lsupaux faca
        achou <- 1
        para j de 1 ate lsupaux faca
            se (vaux[j] = v[i]) entao
                r[j] <- r[j] + 1
                achou <- 0
            fimse
        fimpara
        se (achou = 1) entao
            k <- k + 1
            vaux[k] <- v[i]
            r[k] <- 0
        fimse
    fimpara
    
    para i de 1 ate k faca
        se (i = 1) entao
            maior <- vaux[i]
            vezes <- r[i]
        senao
            se (r[i] > vezes) entao
                maior <- vaux[i]
                vezes <- r[i]
            fimse
        fimse
    fimpara
    
    escreval
    se (vezes = 0) entao
        escreval("Não há números que se repetem abaixo na diagonal secundária.")
    senao
        escreval("O número que vai se repete é", maior," com", vezes," repetição(ões).")
    fimse
    
Fimalgoritmo
