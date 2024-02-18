# Exercício 35

[**Ver Análise**](Analise35.md)

Algoritmo "Q35 - exMatriz"
Var
    i, j, n, k, lsupl, lsupc, maior, menor: inteiro
    m: vetor [1..7, 1..5] de real
    v: vetor [1..35] de inteiro
    s, p, media: real
Inicio
    lsupl <- 7
    lsupc <- 5
    s <- 0
    p <- 1
    
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 5)
            escreva("Insira o", n, "º valor da matriz: ")
            leia(m[i, j])
            
            enquanto ((m[i, j] < 0) ou (m[i, j] > 50)) faca
                escreva("Os valores devem estar entre 0 e 50: ")
                leia(m[i, j])
            fimenquanto
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
    
    escreval
    escreval("Matriz multiplicada por 100: ")
    escreval
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            m[i, j] <- m[i, j] * 100
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    n <- 0
    
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            k <- 0
            
            enquanto (k < m[i, j]) faca
                k <- k + 1
            fimenquanto
            
            se (k = m[i, j]) entao
                n <- n + 1
                v[n] <- k
            fimse
        fimpara
    fimpara
    
    escreval
    
    se (n = 0) entao
        escreval("Não existem inteiros presentes na matriz pós modificação.")
    senao
        escreva("Números inteiros presentes na matriz pós modificação:")
        para i de 1 ate n faca
            se (i = n) entao
                escreval(v[i], ".")
            senao
                escreva(v[i], ",")
            fimse
            
            s <- s + v[i]
            p <- p * v[i]
            
            se (i = 1) entao
                maior <- v[i]
                menor <- v[i]
            senao
                se (v[i] > maior) entao
                    maior <- v[i]
                fimse
                
                se (v[i] < menor) entao
                    menor <- v[i]
                fimse
            fimse
        fimpara
        
        media <- s / n
        escreval
        escreval("Soma dos números inteiros:", s, ".")
        escreval("Produto dos números inteiros:", p, ".")
        escreval("Média dos números inteiros:", media, ".")
        escreval("Maior número inteiro inserido:", maior, ".")
        escreval("Menor número inteiro inserido:", menor, ".")
    fimse
Fimalgoritmo
