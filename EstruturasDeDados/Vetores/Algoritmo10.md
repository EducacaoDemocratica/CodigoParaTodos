# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown



Algoritmo "Q10 - exVetor"
Var
    i, lsup, fat, n: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    para i de 1 ate lsup faca
        fat <- 1
        n <- 1
        enquanto (n < i) faca
            n <- n + 1
            fat <- fat * n
        fimenquanto
        v[i] <- fat
    fimpara
    escreval
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
Fimalgoritmo
