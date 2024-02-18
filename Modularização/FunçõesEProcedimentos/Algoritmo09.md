# Exercício 09

[**Ver Análise**](Analise09.md)

```pascal
Algoritmo "Q9 - exFuncaoProcedimento"

procedimento fatorial(n: inteiro)
Var
    i: inteiro
Inicio
    i <- 0
    f <- 1
    enquanto (i < n) faca
        i <- i + 1
        f <- f * i
    fimenquanto
fimProcedimento

Var
    n: inteiro
    f: real
Inicio
    escreva("Insira um número: ")
    leia(n)
    enquanto (n < 0) faca
        escreva("Insira um valor maior/igual a 0: ")
        leia(n)
    fimenquanto
    fatorial(n)
    escreval
    escreval("O fatorial de", n," é", f,".")
Fimalgoritmo
