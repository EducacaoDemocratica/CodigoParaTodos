# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown
Algoritmo "Q15 - exRepeticao"

Var

    n, s: real
    i, lsup: inteiro

Inicio

    lsup <- 15
    s <- 0
    i <- 1

    escreval("Insira 15 números positivos: ")
    escreval

    enquanto (i <= lsup) faca
        escreva("Insira o", i, "º: ")
        leia(n)

        enquanto (n <= 0) faca
            escreva("O número deve ser positivo: ")
            leia(n)
        fimenquanto

        se (n > 5) entao
            s <- s + n
        fimse

        i <- i + 1

    fimenquanto

    escreval
    escreval("A soma dos números inseridos maiores que 5 é", s, ".")

Fimalgoritmo
