# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - exRepeticao"

Var

    i, lsup: inteiro

Inicio

    i <- 0
    lsup <- 100
    escreval("Pares de 1 a", lsup, ":")
    escreval

    enquanto (i < lsup) faca
        i <- i + 1
        se (i mod 2 = 0) entao
            se (i mod 20 = 0) entao
                escreval
            fimse
            se (i = lsup) entao
                escreval(i, ".")
            senao
                escreva(i, ",")
            fimse
        fimse
    fimenquanto

Fimalgoritmo
