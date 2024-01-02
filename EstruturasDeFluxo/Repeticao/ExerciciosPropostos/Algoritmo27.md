# Exercício 27

[**Ver Análise**](Analise27.md)

```markdown
Algoritmo "Q27 - exRepeticao"

Var
    n, i, fat, j, s: inteiro

Inicio
    i <- 0
    s <- 0

    escreva("Insira um número inteiro positivo: ")
    leia(n)

    enquanto (n <= 0) faca
        escreva("O número deve ser maior que zero: ")
        leia(n)
    fimenquanto

    escreval

    enquanto (i < n) faca
        i <- i + 1

        se (i mod 2 = 0) entao
            s <- s - i
        senao
            s <- s + i
        fimse
    fimenquanto

    escreval("O valor de S é", s, ".")

Fimalgoritmo
