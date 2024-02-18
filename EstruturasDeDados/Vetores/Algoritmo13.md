# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown

Algoritmo "Q13 - exVetor"
Var
    i, lsup: inteiro
    m, n, o: vetor [1..15] de inteiro
Inicio
    lsup <- 15
    m[1] <- 6
    para i de 2 ate lsup faca
        m[i] <- m[i - 1] + 6
    fimpara
    para i de 1 ate lsup faca
        n[i] <- m[i] - 2
    fimpara
    para i de 1 ate lsup faca
        o[i] <- m[i] * n[i]
    fimpara
    escreva("M: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(m[i], ".")
        senao
            escreva(m[i], ",")
        fimse
    fimpara
    escreval
    escreva("N: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(n[i], ".")
        senao
            escreva(n[i], ",")
        fimse
    fimpara
    escreval
    escreva("O: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(o[i], ".")
        senao
            escreva(o[i], ",")
        fimse
    fimpara
    escreval
Fimalgoritmo