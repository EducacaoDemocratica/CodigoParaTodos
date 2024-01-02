# Exercício 21

[**Ver Análise**](Analise21.md)

```markdown
Algoritmo "Q21 - exRepeticao"

Var
    linf, lsup: inteiro

Inicio
    linf <- -1
    lsup <- 8

    escreval("Números inteiros que estão na interseção [-6, 9[.")

    enquanto (linf <= lsup) faca
        se (linf = lsup) entao
            escreval(linf, ".")
        senao
            escreva(linf, ",")
        fimse

        linf <- linf + 1
    fimenquanto

Fimalgoritmo
