# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown

Algoritmo "Q8 - exVetor"
Var
    i, j, lsup: inteiro
    v: vetor [1..100] de inteiro
Inicio
    lsup <- 100
    j <- 1
    i <- 1
    enquanto (i <= lsup) faca
        se (j mod 7 <> 0) entao
            v[i] <- j
            i <- i + 1
        fimse
        j <- j + 1
    fimenquanto
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
