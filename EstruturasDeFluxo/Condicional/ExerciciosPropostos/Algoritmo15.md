---
# Exercício 15

[**Ver Análise**](Analise15.md)
```
Algoritmo "Q15 - exCondicional"

Var
g, a, p: real

Inicio
    escreva("Insira o valor do litro de gasolina: R$")
    leia(g)

    se (g <= 0) entao
        escreval("Erro: valor negativo ou nulo inserido.")
    senao
        escreva("Insira o valor do litro de álcool: R$")
        leia(a)

        se (a <= 0) entao
            escreval("Erro: valor negativo ou nulo inserido.")
        senao
            p <- a/g * 100
            escreval

            se (p < 70) entao
                escreval("É mais vantajoso utilizar álcool.")
            senao
                escreval("É mais vantajoso utilizar gasolina.")
            fimse
        fimse
    fimse
Fimalgoritmo
