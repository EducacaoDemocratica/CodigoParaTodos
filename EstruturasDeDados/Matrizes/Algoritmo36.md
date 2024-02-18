# Exercício 36

[**Ver Análise**](Analise36.md)

Algoritmo "Q36 - exMatriz"
Var
    i, j, n, lsupl, lsupc: inteiro
    m: vetor [1..3, 1..6] de inteiro
    si, m2, m4: real
Inicio
    lsupl <- 3
    lsupc <- 6
    si <- 0
    m2 <- 0
    m4 <- 0
    
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 6)
            escreva("Insira o", n, "º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("Matriz original: ")
    escreval
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            se (j mod 2 = 1) entao
                si <- si + m[i, j]
            fimse
        fimpara
    fimpara
    
    para i de 1 ate lsupl faca
        m2 <- m2 + m[i, 2]
        m4 <- m4 + m[i, 4]
    fimpara
    
    m2 <- m2 / i
    m4 <- m4 / i
    
    para i de 1 ate lsupl faca
        m[i, 6] <- m[i, 1] + m[i, 2]
        m[i, 6] <- m[i, 1] + m[i, 2]
    fimpara
    
    escreval
    escreval("Soma dos elementos das colunas ímpares:", si, ".")
    escreval("Média da 2ª coluna:", m2, ".")
    escreval("Média da 4ª coluna:", m4, ".")
    escreval
    escreval("Matriz pós modificação na 6ª coluna: ")
    escreval
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
