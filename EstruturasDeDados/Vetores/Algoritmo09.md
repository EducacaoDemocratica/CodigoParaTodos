# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown


Algoritmo "Q9 - exVetor"
Var
    i, j, lsup: inteiro
    v: vetor [1..100] de inteiro
Inicio
    lsup <- 500
    j <- 1
    i <- 0
    enquanto (j <= lsup) faca
        se (j mod 5 = 0) entao
            i <- i + 1
            v[i] <- j
        fimse
        j <- j + 1
    fimenquanto
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

