# Exercício 35

[**Ver Análise**](Analise35.md)

```markdown


Algoritmo "Q35 - exVetor"
Var
    i, lsup, a1, r: inteiro
    s: real
    pa: vetor [1..10] de real
    tipoPa: caractere

Inicio
    lsup <- 10
    s <- 0

    escreva("Insira o primeiro termo: ")
    leia(a1)

    escreva("Insira a razão: ")
    leia(r)

    se (r > 0) entao
        tipoPa <- "crescente."
    senao
        se (r = 0) entao
            tipoPa <- "constante."
        senao
            tipoPa <- "decrescente."
        fimse
    fimse

    para i de 1 ate lsup faca
        pa[i] <- a1 + ((i - 1) * r)
        s <- s + pa[i]
    fimpara

    escreval
    escreval("Progressão aritmética ", tipoPa)

    escreva("10 primeiros termos:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(pa[i], ".")
        senao
            escreva(pa[i], ",")
        fimse
    fimpara

    escreval("Soma dos elementos:", s, ".")
Fimalgoritmo
