# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown
Algoritmo "Q14 - exRepeticao"

Var

    n, aux: inteiro

Inicio

    aux <- 0
    escreva("Insira um número inteiro positivo: ")
    leia(n)

    enquanto (n <= 0) faca
        escreva("O número deve ser maior que zero: ")
        leia(n)
    fimenquanto

    escreval
    escreva("Divisores de", n, ": ")

    enquanto (aux < n) faca
        aux <- aux + 1

        se (n mod aux = 0) entao
            se (n = aux) entao
                escreval(aux, ".")
            senao
                escreva(aux, ",")
            fimse
        fimse

    fimenquanto

Fimalgoritmo
