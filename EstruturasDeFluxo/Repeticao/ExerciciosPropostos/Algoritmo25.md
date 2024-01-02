# Exercício 25

[**Ver Análise**](Analise25.md)

```markdown
Algoritmo "Q25 - exRepeticao"

Var

    n, s, i: inteiro

Inicio

    i <- -1
    s <- 0

    escreva("Insira um número inteiro positivo: ")
    leia(n)

    enquanto (n <= 0) faca
        escreva("O número deve ser maior que zero: ")
        leia(n)
    fimenquanto

    escreval

    enquanto (i < (n*2 - 1)) faca
        i <- i + 2
        s <- s + i
    fimenquanto

    escreval("O valor de S é", s, ".")

Fimalgoritmo
