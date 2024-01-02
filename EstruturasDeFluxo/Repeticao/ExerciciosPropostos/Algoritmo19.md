# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - exRepeticao"

Var

    n, k: inteiro
    ex1, ex2: real

Inicio

    ex1 <- 0
    ex2 <- 0
    k <- 0

    escreva("Insira um número inteiro maior que um: ")
    leia(n)

    enquanto (n < 2) faca
        escreva("O número deve ser no mínimo igual a dois: ")
        leia(n)
    fimenquanto

    enquanto (k < n) faca
        k <- k + 1
        ex1 <- ex1 + k
        ex2 <- ex2 + k^3
    fimenquanto

    ex1 <- ex1 ^ 2

    escreval
    escreval("Resultado da expressão (k1 + k2 + ... + kn)²:", ex1, ".")
    escreval("Resultado da expressão (k1³ + k2³ + ... + kn³):", ex2, ".")
    escreval

Fimalgoritmo
