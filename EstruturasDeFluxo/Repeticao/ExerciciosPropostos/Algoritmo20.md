# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown
Algoritmo "Q20 - exRepeticao"

Var

    linf, lsup, aux: inteiro

Inicio

    linf <- -6
    lsup <- 18
    aux <- 1

    escreval("Números inteiros que estão no intervalo [-2, 18] U [-6, 9[:")
    escreval

    enquanto (linf <= lsup) faca
        se (aux mod 15 = 0) entao
            escreval
        fimse

        se (linf = lsup) entao
            escreval(linf, ".")
        senao
            escreva(linf, ",")
        fimse

        linf <- linf + 1
        aux <- aux + 1
    fimenquanto

Fimalgoritmo
