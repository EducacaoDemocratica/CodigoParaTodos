# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown


Algoritmo "Q5 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..10] de real
Inicio
    lsup <- 10
    para i de 1 ate lsup faca
        v[i] <- ((i * 2) - 1) ^ 2
    fimpara
    lsup <- i
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
