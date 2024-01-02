# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - exRepeticao"

Var

    i, lsup: inteiro

Inicio

    i <- 0
    lsup <- 100
    escreval("Os múltiplos de 7 de 1 a", lsup, ":")
    escreval

    enquanto (i < lsup) faca
        i <- i + 1
        se (i mod 7 = 0) entao
            se ((i + 7) > lsup) entao
                escreval(i, ".")
            senao
                escreva(i, ",")
            fimse
        fimse
    fimenquanto

Fimalgoritmo
