# Exercício 06

[**Ver Análise**](Analise06.md)
```
Algoritmo "Q6 - exCondicional"

Var
n: inteiro

Inicio
    escreva("Insira um número: ")
    leia(n)
    escreval

    se ((n mod 3 = 0) ou (n mod 5 = 0)) entao
        se (n mod 5 <> 0) entao
            escreval(n, " é múltiplo de 3.")
        senao
            se (n mod 3 <> 0) entao
                escreval(n, " é múltiplo de 5.")
            senao
                escreval(n, " é múltiplo de ambos.")
            fimse
        fimse
    senao
        escreval(n, " não é múltiplo de 3 ou 5.")
    fimse

Fimalgoritmo
