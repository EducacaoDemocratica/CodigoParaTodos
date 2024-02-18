# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown


Algoritmo "Q12 - exVetor"
Var
    i, s, lsup: inteiro
    a: vetor [1..6] de inteiro
Inicio
    lsup <- 6
    a[1] <- 1
    a[2] <- 0
    a[3] <- 5
    a[4] <- -2
    a[5] <- -5
    a[6] <- 7
    escreva("Vetor original: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(a[i], ".")
        senao
            escreva(a[i], ",")
        fimse
    fimpara
    s <- a[1] + a[2] + a[6]
    escreval("Soma da 1ª, 2ª e 6ª posição:", s)
    a[4] <- 100
    escreva("Vetor após mudança na 4ª posição: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(a[i], ".")
        senao
            escreva(a[i], ",")
        fimse
    fimpara
Fimalgoritmo
