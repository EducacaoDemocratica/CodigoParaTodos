# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown

Algoritmo "Q2 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    para i de 1 ate lsup faca
        v[i] <- (i * 2)
    fimpara
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
Fimalgoritmo
