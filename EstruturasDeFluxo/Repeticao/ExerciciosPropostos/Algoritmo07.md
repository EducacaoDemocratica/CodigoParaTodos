# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - exRepeticao"

Var

    i, lsup: inteiro

Inicio

    i <- 30
    lsup <- 100
    escreval("Números de 30 a 100 em sequência:")
    escreval

    enquanto (i <= lsup) faca
        se (i mod 10 = 0) entao
            escreval
        fimse
        se (i = lsup) entao
            escreval(i, ".")
        senao
            escreva(i, ",")
        fimse
        i <- i + 1
    fimenquanto

Fimalgoritmo
