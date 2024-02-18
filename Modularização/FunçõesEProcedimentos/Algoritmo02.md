# Exercício 02

[**Ver Análise**](Analise02.md)

```pascal
Algoritmo "Q2 - exFuncaoProcedimento"

funcao converteParaKelvin(c: real) : real
Var
Inicio
    retorne c + 273.15
fimFuncao

funcao converteParaFahrenheit(c: real) : real
Var
Inicio
    retorne c * 1.8 + 32
fimFuncao

funcao converteParaReaumur(c: real) : real
Var
Inicio
    retorne c * 0.8
fimFuncao

funcao converteParaRankine(c: real) : real
Var
Inicio
    retorne c * 1.8 + 32 + 459.67
fimFuncao

Var
    c: real
Inicio
    escreva("Insira uma temperatura em Celsius: ")
    leia(c)
    enquanto (c < -273.15) faca
        escreva("Insira um valor maior que -273.15: ")
        leia(c)
    fimenquanto
    escreval
    escreval("Temperatura em Celsius:", c,"º C.")
    escreval("Temperatura em Kelvin:", converteParaKelvin(c),"K.")
    escreval("Temperatura em Réaumur:", converteParaReaumur(c),"º Re.")
    escreval("Temperatura em Rankine:", converteParaRankine(c),"Ra.")
    escreval("Temperatura em Fahrenheit:", converteParaFahrenheit(c),"º F.")
Fimalgoritmo
