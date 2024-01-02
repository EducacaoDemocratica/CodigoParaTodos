# Exercício 14

[**Ver Análise**](Analise14.md)

Algoritmo "Q14 - exCondicional"

Var
p, f, t: real

Inicio
    escreva("Insira o valor do produto: R$")
    leia(p)

    se (p <= 0) entao
        escreval("Erro: valor inválido.")
    senao
        escreva("Insira o valor fornecido pelo cliente: R$")
        leia(f)

        se (f <= 0) entao
            escreval("Erro: valor inválido.")
        senao
            escreval
            escreval("Valor do produto: R$", p,".")
            escreval("Valor pago pelo cliente: R$", f,".")

            se (f > p) entao
                t <- f - p
                escreval("Valor do troco: R$", t,".")
            senao
                se (f = p) entao
                    escreval("A compra não possui troco.")
                senao
                    t <- p - f
                    escreval("São necessários mais R$", t," para realizar a compra.")
                fimse
            fimse
        fimse
    fimse
Fimalgoritmo
