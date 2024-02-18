# Exercício 25

[**Ver Análise**](Analise25.md)

```markdown

Algoritmo "Q25 - exVetor"
Var
    i, q, lsup: inteiro
    s: real
    v: vetor [1..100] de real
Inicio
    lsup <- 100
    s <- 0
    q <- 0
    para i de 1 ate lsup faca
        escreva("Insira o ", i, "º número: ")
        leia(v[i])
        se (v[i] < 0) entao
            q <- q + 1
        senao
            s <- s + v[i]
        fimse
    fimpara
    escreval
    escreval("Foram inseridos ", q, " números negativos.")
    escreval("A soma dos números positivos é igual a ", s, ".")
Fimalgoritmo