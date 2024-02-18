# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown

Algoritmo "Q4 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..101] de inteiro
Inicio
    lsup <- 101
    para i de 1 ate lsup faca
        v[i] <- 200 - (i - 1)
    fimpara
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
