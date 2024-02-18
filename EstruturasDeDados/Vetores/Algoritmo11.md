# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown

Algoritmo "Q11 - exVetor"
Var
    i, lsup, aux1, aux2, aux3: inteiro
    v: vetor [1..50] de inteiro
Inicio
    lsup <- 50
    aux1 <- -1
    aux2 <- 1
    para i de 1 ate lsup faca
        aux3 <- aux1 + aux2
        aux1 <- aux2
        aux2 <- aux3
        v[i] <- aux3
    fimpara
    escreval
    para i de 1 ate lsup faca
        se (i mod 10 = 1) entao
            escreval
        fimse
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
Fimalgoritmo
