# Exercício 08

[**Ver Análise**](Analise08.md)

```pascal
Algoritmo "Q8 - exFuncaoProcedimento"

funcao trocaNumero(n: inteiro): inteiro
Var
Inicio
    retorne n
fimFuncao

procedimento imprimir(x, y: inteiro)
Var
Inicio
    escreval("x =", x)
    escreval("y =", y)
fimProcedimento

Var
    x, y, xaux: inteiro
Inicio
    escreva("Insira o valor de x: ")
    leia(x)
    xaux <- x
    escreva("Insira o valor de y: ")
    leia(y)
    enquanto (x = y) faca
        escreva("y deve ser diferente de x: ")
        leia(y)
    fimenquanto
    escreval
    escreval("ANTES DA TROCA:")
    imprimir(x, y)
    x <- trocaNumero(y)
    y <- trocaNumero(xaux)
    escreval
    escreval("DEPOIS DA TROCA:")
    imprimir(x, y)
Fimalgoritmo
