# Exercício 11

[**Ver Análise**](Analise11.md)

```pascal
Algoritmo "Q11 - exFuncaoProcedimento"

procedimento desenho1(n: inteiro)
Var
    i, j: inteiro
Inicio
    para i de 1 ate n faca
        para j de 1 ate n faca
            se ((i = j) ou (i = n)) entao
                escreva(" * ")
            senao
                escreva(" ")
            fimse
        fimpara
        escreval
    fimpara
fimProcedimento

procedimento desenho2(n: inteiro)
Var
    i, j: inteiro
Inicio
    para i de 2 ate (n + 1) faca
        escreva(i, " ")
    fimpara
    escreval
    para i de n ate 2 passo -1 faca
        para j de 1 ate n faca
            se (j = n) entao
                escreval(i)
            senao
                escreva(" ")
            fimse
        fimpara
    fimpara
    para i de n ate 1 passo -1 faca
        escreva(i, " ")
    fimpara
fimProcedimento

Var
    n: inteiro
Inicio
    escreva("Insira um número: ")
    leia(n)
    enquanto (n <= 0) faca
        escreva("Insira um valor maior que 0: ")
        leia(n)
    fimenquanto
    escreval
    escreval("1º padrão: ")
    escreval
    desenho1(n)
    escreval
    escreval
    escreval("2º padrão: ")
    escreval
    desenho2(n)
    escreval
Fimalgoritmo
