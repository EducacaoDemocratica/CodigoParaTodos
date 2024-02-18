# Exercício 21

[**Ver Análise**](Analise21.md)

Algoritmo "Q21 - exMatriz"
Var
    i, j, n, aux, lsup: inteiro
    m: vetor [1..4, 1..4] de inteiro
    v: vetor [1..16] de inteiro
Inicio
    lsup <- 4
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            v[n] <- m[i, j]
        fimpara
    fimpara
    escreval
    escreval("Matriz antes da ordenação: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    escreval
    para j de ((lsup * lsup) - 1) ate 1 passo -1 faca
        para i de 1 ate j faca
            se (v[i] > v[i + 1]) entao
                aux <- v[i]
                v[i] <- v[i + 1]
                v[i + 1] <- aux
            fimse
        fimpara
    fimpara
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 4)
            m[i, j] <- v[n]
        fimpara
    fimpara
    escreval("Matriz após a ordenação das colunas: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
