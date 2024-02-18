# Exercício 26

[**Ver Análise**](Analise26.md)

```markdown

Algoritmo "Q26 - exVetor"
Var
    i, c, lsup: inteiro
    v, vi: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    c <- 0
    para i de 1 ate lsup faca
        escreva("Insira o ", i, "º número: ")
        leia(v[i])
        enquanto ((v[i] < 0) ou (v[i] > 50)) faca
            escreva("O número deve pertencer ao intervalo [0, 50]: ")
            leia(v[i])
        fimenquanto
    fimpara
    escreval
    para i de 1 ate lsup faca
        se (v[i] mod 2 = 1) entao
            c <- c + 1
            vi[c] <- v[i]
        fimse
    fimpara
    escreva("Vetor original: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
    escreva("Vetor somente com os ímpares: ")
    para i de 1 ate c faca
        se (i = c) entao
            escreval(vi[i], ".")
        senao
            escreva(vi[i], ",")
        fimse
    fimpara
Fimalgoritmo