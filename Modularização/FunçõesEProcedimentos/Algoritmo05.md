# Exercício 05

[**Ver Análise**](Analise05.md)

```pascal
Algoritmo "Q5 - exFuncaoProcedimento"

funcao leNumero(): real
Var
    n: real
Inicio
    leia(n)
    enquanto (n <= 0) faca
        escreva("Insira um valor maior que 0: ")
        leia(n)
    fimenquanto
    retorne n
fimFuncao

procedimento calculaIMC(p, a: real)
Var
Inicio
    imc <- p/(a ^ 2)
fimProcedimento

Var
    p, a, imc: real
Inicio
    escreva("Insira o valor do peso (kg): ")
    p <- leNumero()
    escreva("Insira o valor da altura (m): ")
    a <- leNumero()
    calculaIMC(p, a)
    escreval
    escreval("O valor do IMC é ", imc:6:2,".")
Fimalgoritmo
