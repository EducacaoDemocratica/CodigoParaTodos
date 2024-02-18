# Exercício 30

[**Ver Análise**](Analise30.md)

```markdown

Algoritmo "Q30 - exVetor"
Var
    i, lsup, maior: inteiro
    v: vetor [1..10] de inteiro
    vaux: vetor [1..10] de real
Inicio
    lsup <- 10
    maior <- 0
    
    para i de 1 ate lsup faca
        escreva("Insira o", i," número: ")
        leia(v[i])
        
        enquanto (v[i] <= 0) faca
            escreva("Insira um número diferente de 0: ")
            leia(v[i])
        fimenquanto
    fimpara
    
    para i de 1 ate lsup faca
        se (i mod 2 = 0) entao
            vaux[i] <- v[i] / 2
        senao
            vaux[i] <- v[i] * 3
        fimse
    fimpara
    
    escreval
    
    escreva("Primeiro vetor:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
    
    escreva("Segundo vetor:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(vaux[i], ".")
        senao
            escreva(vaux[i], ",")
        fimse
    fimpara
Fimalgoritmo
