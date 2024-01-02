# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - exRepeticao"

Var
    i, lsup: inteiro

Inicio
    i <- 0
    lsup <- 5
    escreval("Inteiros de 1 a", lsup, ":")
    escreval

    enquanto (i < lsup) faca
        i <- i + 1
        se (i = lsup) entao
            escreval(i, ".")
        senao
            escreva(i, ",")
        fimse
    fimenquanto

Fimalgoritmo
