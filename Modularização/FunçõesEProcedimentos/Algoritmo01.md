# Exercício 01

[**Ver Análise**](Analise1.md)

```pascal
Algoritmo "Q1 - exFuncaoProcedimento"

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

funcao calculaCavalos(m, h, t: real) : real
Var
Inicio
    retorne (m * h / t)/745.7
fimFuncao

Var
    t, m, h, cavalos: real
Inicio
    escreva("Insira o valor da massa: ")
    m <- leNumero()
    escreva("Insira o valor da altura: ")
    h <- leNumero()
    escreva("Insira a quantidade de segundos: ")
    t <- leNumero()
    cavalos <- calculaCavalos(m, h, t)
    escreval
    escreval("A quantidade de cavalos necessários é de ", cavalos:6:2, " cavalos.")
Fimalgoritmo
