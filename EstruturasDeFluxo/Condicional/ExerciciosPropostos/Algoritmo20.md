# Exercício 20

[**Ver Análise**](Analise20.md)

Algoritmo "Q20 - exCondicional"

Var
x, fx: real

Inicio
    escreva("Insira o valor de x: ")
    leia(x)

    se (((x^2) + 1) = 0) entao
        escreval("f(x) é indefinido (divisão por 0).")
    senao
        fx <- ((x^3) - 1) / ((x^2) + 1)
        escreval("O valor de f(",x," ) é ", fx,".")
    fimse

Fimalgoritmo
