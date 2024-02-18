# Exercício 06

[**Ver Análise**](Analise06.md)

```pascal
Algoritmo "Q6 - exFuncaoProcedimento"

funcao leNumero(): real
Var
    n: real
Inicio
    leia (n)
    enquanto (n <= 0) faca
        escreva("Insira um valor maior que 0: ")
        leia(n)
    fimenquanto
    retorne n
fimFuncao

funcao calculaIMC(p, a: real): real
Var
Inicio
    retorne p/(a ^ 2)
fimFuncao

Var
    p, a, imc: real
Inicio
    escreva("Insira o valor do peso (kg): ")
    p <- leNumero()
    escreva("Insira o valor da altura (m): ")
    a <- leNumero()
    imc <- calculaIMC(p, a)
    escreval
    escreval("O valor do IMC é ", imc:6:2,".")
Fimalgoritmo
