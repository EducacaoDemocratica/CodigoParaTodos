# Exercício 06

[**Ver Análise**](Analise06.md)

```
Algoritmo "Q6 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..50] de inteiro
Inicio
    lsup <- 50
    para i de 1 ate lsup faca
        v[i] <- (i * 2) - 1
    fimpara
    lsup <- i
    para i de 1 ate lsup faca
        se (i mod 10 = 1) entao
            escreval
        fimse
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
Fimalgoritmo
