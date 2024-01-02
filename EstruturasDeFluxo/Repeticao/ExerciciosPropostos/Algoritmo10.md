# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown
Algoritmo "Q10 - exRepeticao"

Var

    i, k, aux, lsup: inteiro

Inicio

    i <- 0
    lsup <- 9

    enquanto (i < lsup) faca
        i <- i + 1
        escreval("Tabuada do", i, ": ")
        escreval

        k <- 0
        aux <- 0

        enquanto (aux <= lsup) faca
            aux <- aux + 1
            k <- k + i
            se (aux = (lsup + 1)) entao
                escreval(k, ".")
            senao
                escreva(k, ",")
            fimse
        fimenquanto

        escreval
    fimenquanto

Fimalgoritmo
