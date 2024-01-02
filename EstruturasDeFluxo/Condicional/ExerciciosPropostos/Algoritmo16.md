---
# Exercício 16

[**Ver Análise**](Analise16.md)
```markdown
Algoritmo "Q16 - exCondicional"

Var

    x, y: real

Inicio

    escreva("Insira o valor de x: ")
    leia(x)
    escreva("Insira o valor de y: ")
    leia(y)
    escreval

    escreva("O par ordenado (", x," ,", y," ) está no " )

    se ((x = 0) ou (y = 0)) entao
        escreval("eixo do plano.")
    senao
        se ((x > 0) e (y > 0)) entao
            escreval("1º quadrante.")
        senao
            se ((x < 0) e (y > 0)) entao
                escreval("2º quadrante.")
            senao
                se ((x < 0) e (y < 0)) entao
                    escreval("3º quadrante.")
                senao
                    escreval("4º quadrante.")
                fimse
            fimse
        fimse
    fimse

Fimalgoritmo

