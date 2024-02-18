# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown


Algoritmo "Q14 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número: ")
        leia(v[i])
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

