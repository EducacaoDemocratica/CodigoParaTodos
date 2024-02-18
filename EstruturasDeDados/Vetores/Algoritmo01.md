# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    para i de 1 ate lsup faca
        v[i] <- i
    fimpara
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
Fimalgoritmo