# Exercício 31

[**Ver Análise**](Analise31.md)

```markdown

Algoritmo "Q31 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..10] de inteiro
    r: vetor [1..10] de real
Inicio
    lsup <- 10
    
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número: ")
        leia(v[i])
        
        se (v[i] < 0) entao
            r[i] <- -1
        senao
            r[i] <- (v[i]^(1/2))
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
    
    escreva("Raízes:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(r[i]:6:2, ".")
        senao
            escreva(r[i]:6:2, ",")
        fimse
    fimpara
Fimalgoritmo
