# Exercício 04

[**Ver Análise**](Analise04.md)

```pascal
Algoritmo "Q4 - exFuncaoProcedimento"

funcao calculaVolume(r: real): real
Var
Inicio
    retorne (4/3 * pi * r ^ 3)
fimFuncao

Var
    r, v: real
Inicio
    escreva("Insira o valor do raio: ")
    leia(r)
    enquanto (r <= 0) faca
        escreva("Insira um valor maior que 0: ")
        leia(r)
    fimenquanto
    v <- calculaVolume(r)
    escreval
    escreval("O volume da esfera de raio", r," é ", v:6:2,".")
Fimalgoritmo
