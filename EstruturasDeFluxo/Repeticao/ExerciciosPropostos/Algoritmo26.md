# Exercício 26

[**Ver Análise**](Analise26.md)

```markdown
Algoritmo "Q26 - exRepeticao"

Var
    n, i: inteiro
    s: real

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

    enquanto (i < (n*2 - 1)) faca
        i <- i + 2
        s <- s + (i ^ (1/2))
    fimenquanto

    escreval("O valor de S é", s, ".")

Fimalgoritmo
