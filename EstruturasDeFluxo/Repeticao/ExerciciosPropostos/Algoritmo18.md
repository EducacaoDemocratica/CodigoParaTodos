# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown
Algoritmo "Q18 - exRepeticao"

Var

    i, lsup, n, s: inteiro

Inicio

    lsup <- 100
    s <- 0
    i <- 1

    enquanto (i <= lsup) faca
        escreva("Insira um número: ")
        leia(n)
        se (n mod 2 = 0) entao
            s <- s + n
        fimse
        i <- i + 1
    fimenquanto

    escreval
    escreval("A soma dos números pares inseridos é", s, ".")

Fimalgoritmo
