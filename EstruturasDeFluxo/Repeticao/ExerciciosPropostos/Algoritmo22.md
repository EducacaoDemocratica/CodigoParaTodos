# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown
Algoritmo "Q22 - exRepeticao"

Var

    aux, n, maior: inteiro

Inicio

    n <- 0
    aux <- 0

    enquanto (n <> -1) faca
        se (aux = 1) entao
            maior <- n
        senao
            se (n > maior) entao
                maior <- n
            fimse
        fimse

        escreva("Insira n: ")
        leia(n)
        aux <- aux + 1
    fimenquanto

    escreval

    se (aux = 1) entao
        escreval("Nenhum número válido (maior que -1) foi inserido no conjunto.")
    senao
        escreval("O maior número do conjunto é", maior,".")
    fimse

Fimalgoritmo
