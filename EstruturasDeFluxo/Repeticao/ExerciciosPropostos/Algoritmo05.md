# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - exRepeticao"

Var

    i, n, k: inteiro

Inicio

    i <- 0
    k <- 0
    escreva("Insira um número positivo: ")
    leia(n)

    enquanto (n <= 0) faca
        escreva("O número deve ser maior que 0: ")
        leia(n)
    fimenquanto

    escreval
    escreval("Os", n, " primeiros números pares:")
    escreval

    enquanto (i < n) faca
        k <- k + 1
        se (k mod 2 = 0) entao
            i <- i + 1
            se (i mod 10 = 0) entao
                escreval
           
