# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..100] de inteiro
Inicio
    lsup <- 100
    para i de 1 ate lsup faca
        v[i] <- (i * 2) - 1
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
