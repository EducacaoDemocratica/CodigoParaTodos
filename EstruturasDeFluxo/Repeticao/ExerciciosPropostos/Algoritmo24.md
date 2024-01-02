# Exercício 24

[**Ver Análise**](Analise24.md)

```markdown
Algoritmo "Q24 - exRepeticao"

Var

    n, s, i: inteiro

Inicio

    i <- 0
    s <- 0

    escreva("Insira um número inteiro positivo: ")
    leia(n)

    enquanto (n <= 0) faca
        escreva("O número deve ser maior que zero: ")
        leia(n)
    fimenquanto

    escreval

    enquanto (i < n) faca
        i <- i + 1
        s <- s + i
    fimenquanto

    escreval("O valor de S é", s, ".")

Fimalgoritmo
