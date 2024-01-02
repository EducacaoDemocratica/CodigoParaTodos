# Exercício 07

[**Ver Análise**](Analise07.md)
```
Algoritmo "Q7 - exCondicional"

Var
n, r: real

Inicio
    escreva("Insira um número: ")
    leia(n)
    escreval

    se (n < 0) entao
        escreval("O número é negativo, portanto não possui raiz quadrada real.")
    senao
        r <- n ^ (1/2)
        escreval("A raiz quadrada de", n," é", r,".")
    fimse

Fimalgoritmo
