# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown
Algoritmo "Q23 - exRepeticao"

Var

    t: inteiro
    a, b: real

Inicio

    a <- 1.76
    b <- 2.12
    t <- 0

    enquanto (a < b) faca
        a <- a + 0.12
        b <- b + 0.05
        t <- t + 1
    fimenquanto

    escreval("Serão necessários", t, " anos para que A seja maior que B.")

Fimalgoritmo
