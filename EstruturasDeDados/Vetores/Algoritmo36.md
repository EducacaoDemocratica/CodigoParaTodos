# Exercício 36

[**Ver Análise**](Analise36.md)

```markdown


Algoritmo "Q36 - exVetor"
Var
    i, lsup: inteiro
    a1, q: real
    s: real
    pg: vetor [1..10] de real
    tipoPg: caractere

Inicio
    lsup <- 10
    s <- 0

    escreva("Insira o primeiro termo: ")
    leia(a1)

    enquanto (a1 = 0) faca
        escreva("Insira um número diferente de 0: ")
        leia(a1)
    fimenquanto

    escreva("Insira a razão: ")
    leia(q)

    enquanto (q = 0) faca
        escreva("Insira um número diferente de 0: ")
        leia(q)
    fimenquanto

    se (((q > 0) e (q < 1)) ou ((q > 1) e (a1 < 0))) entao
        tipoPg <- "decrescente."
    senao
        se (q = 1) entao
            tipoPg <- "constante."
        senao
            se (q > 1) entao
                tipoPg <- "crescente."
            senao
                tipoPg <- "alternada."
            fimse
        fimse
    fimse

    para i de 1 ate lsup faca
        pg[i] <- a1 * q ^(i - 1)
        s <- s + pg[i]
    fimpara

    escreval
    escreval("Progressão geométrica ", tipoPg)

    escreva("10 primeiros termos:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(pg[i], ".")
        senao
            escreva(pg[i], ",")
        fimse
    fimpara

    escreval("Soma dos elementos:", s, ".")
Fimalgoritmo
