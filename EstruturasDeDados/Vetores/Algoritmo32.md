# Exercício 32

[**Ver Análise**](Analise32.md)

```markdown

Algoritmo "Q32 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..8] de inteiro
    l: vetor [1..8] de real
Inicio
    lsup <- 8
    
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número: ")
        leia(v[i])
        
        se (v[i] <= 0) entao
            l[i] <- -1
        senao
            l[i] <- log(v[i])
        fimse
    fimpara
    
    escreval
    
    escreva("Valores:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
    
    escreva("Logaritmos:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(l[i]:6:2, ".")
        senao
            escreva(l[i]:6:2, ",")
        fimse
    fimpara
Fimalgoritmo
