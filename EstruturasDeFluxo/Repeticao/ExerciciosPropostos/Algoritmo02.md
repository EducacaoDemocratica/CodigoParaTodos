# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - exRepeticao"

Var

    i, lsup: inteiro

Inicio

    i <- 0
    lsup <- 100
    escreval("Inteiros de 1 a", lsup, ":")
    escreval

    enquanto (i < lsup) faca
        i <- i + 1
        se (i mod 10 = 0) entao
            escreval
        fimse

        se (i = lsup) entao
            escreval(i, ".")
        senao
            escreva(i, ",")
        fimse
    fimenquanto

Fimalgoritmo
