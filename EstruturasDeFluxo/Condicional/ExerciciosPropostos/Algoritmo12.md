# Exercício 12

[**Ver Análise**](Analise12.md)
```markdown
Algoritmo "Q12 - exCondicional"

Var

    l1, l2, l3: inteiro
    t: logico

Inicio

    t <- verdadeiro
    escreva("Insira o valor para um lado de um triângulo: ")
    leia(l1)

    se (l1 <= 0) entao
        escreva("Não há lado negativo ou nulo em um triângulo.")
    senao
        escreva("Insira o valor para um lado: ")
        leia(l2)

        se (l2 <= 0) entao
            escreval("Não há lado negativo ou nulo.")
        senao
            escreva("Insira o valor para um lado: ")
            leia(l3)

            se (l3 <= 0) entao
                escreval("Não há lado negativo ou nulo.")
            senao
                escreval

                se ((l1 > (l2 + l3)) ou (l2 > (l1 + l3)) ou (l3 > (l1 + l2))) entao
                    t <- falso
                fimse

                se (t = verdadeiro) entao
                    se ((l1 = l2) ou (l1 = l3) ou (l2 = l3)) entao
                        escreval("Erro: medidas iguais.")
                    senao
                        escreval("Os lados do triângulo são:")
                        escreval("Lado 1: ", l1,".")
                        escreval("Lado 2: ", l2,".")
                        escreval("Lado 3: ", l3,".")

                        se ((l1 > l2) e (l1 > l3)) entao
                            escreval("A hipotenusa é o 1º lado com medida", l1,".")
                        senao
                            se ((l2 > l1) e (l2 > l3)) entao
                                escreval("A hipotenusa é o 2º lado com medida", l2,".")
                            senao
                                escreval("A hipotenusa é o 3º lado com medida", l3,".")
                            fimse
                        fimse
                    fimse
                senao
                    escreval("Os lados não podem formar um triângulo.")
                fimse
            fimse
        fimse
    fimse
Fimalgoritmo
