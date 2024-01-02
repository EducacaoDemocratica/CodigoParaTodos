---
# Exercício 19

[**Ver Análise**](Analise19.md)
```
Algoritmo "Q19 - exCondicional"

Var
x, fx: real

Inicio
    escreva("Insira o valor de x: ")
    leia(x)

    se ((2 - x) = 0) entao
        escreval("f(x) é indefinido (divisão por 0).")
    senao
        fx <- (8/(2 - x))
        escreval("O valor de f(",x," ) é ", fx,".")
    fimse

Fimalgoritmo
