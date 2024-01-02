# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - exRepeticao"

Var

    i, linf: inteiro

Inicio

    i <- 100
    linf <- 30
    escreval("Números de 100 a 30 em sequência decrescente:")
    escreval

    enquanto (i >= linf) faca
        se (i mod 10 = 0) entao
            escreval
        fimse
        se (i = linf) entao
            escreval(i, ".")
        senao
            escreva(i, ",")
        fimse
        i <- i - 1
    fimenquanto

Fimalgoritmo
