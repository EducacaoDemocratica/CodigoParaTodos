---
# Exercício 18

[**Ver Análise**](Analise18.md)
``` markdown
Algoritmo "Q18 - exCondicional"

Var

    x, y: real

Inicio

    escreva("Insira o valor de x: ")
    leia(x)

    se (x <= 1) entao
        y <- 1
    senao
        se (x <= 2) entao
            y <- 2
        senao
            se (x <= 3) entao
                y <- x^2
            senao
                y <- x^3
            fimse
        fimse
    fimse

    escreval("O valor de f(",x," ) é igual a", y)
Fimalgoritmo
