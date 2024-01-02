# Exercício 17

[**Ver Análise**](Analise17.md)

Algoritmo "Q17 - exCondicional"

Var
c, t, a, vf: real

Inicio
    c <- 450
    escreval("Selecione o seu animal:")
    escreval("1 - Gato | 2 - Papagaio | 3 - Cão | 4 - Nenhum")
    leia(a)

    se (a < 1) ou (a > 4) entao
        escreval("Opção inválida.")
    senao
        se (a = 1) entao
            t <- 30
        senao
            se (a = 2) entao
                t <- 12
            senao
                se (a = 3) entao
                    t <- 50
                senao
                    t <- -20
                fimse
            fimse
        fimse
    fimse

    vf <- c + t
    escreval
    escreval("O valor final a ser pago é R$", vf,".")
    fimse

Fimalgoritmo
