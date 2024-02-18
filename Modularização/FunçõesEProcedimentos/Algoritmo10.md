# Exercício 10

[**Ver Análise**](Analise10.md)

```pascal
Algoritmo "Q10 - exFuncaoProcedimento"

funcao fatorial(n: inteiro): real
Var
    i: inteiro
    f: real
Inicio
    i <- 0
    f <- 1
    enquanto (i < n) faca
        i <- i + 1
        f <- f * i
    fimenquanto
    retorne f
fimFuncao

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
    f <- fatorial(n)
    escreval
    escreval("O fatorial de", n," é", f,".")
Fimalgoritmo
