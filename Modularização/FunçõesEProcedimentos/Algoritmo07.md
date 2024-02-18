# Exercício 07

[**Ver Análise**](Analise07.md)

```pascal
Algoritmo "Q7 - exFuncaoProcedimento"

procedimento trocaNumero()
Var
    aux: inteiro
Inicio
    aux <- x
    x <- y
    y <- aux
fimProcedimento

procedimento imprimir(x, y: inteiro)
Var
Inicio
    escreval("x =", x)
    escreval("y =", y)
fimProcedimento

Var
    x, y: inteiro
Inicio
    escreva("Insira o valor de x: ")
    leia(x)
    escreva("Insira o valor de y: ")
    leia(y)
    enquanto (x = y) faca
        escreva("y deve ser diferente de x: ")
        leia(y)
    fimenquanto
    escreval
    escreval("ANTES DA TROCA:")
    imprimir(x, y)
    trocaNumero()
    escreval
    escreval("DEPOIS DA TROCA:")
    imprimir(x, y)
Fimalgoritmo
