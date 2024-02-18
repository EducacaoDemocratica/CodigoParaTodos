# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - Matriz"
Var
    m: vetor [1..2, 1..2] de inteiro
    i, j, lsup, p, dp, ds, det: inteiro
Inicio
    lsup <- 2
    dp <- 1
    ds <- 1
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * 2)
            escreva("Insira o", p,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    para j de 1 ate lsup faca
        para i de 1 ate lsup faca
            se (i = j) entao
                dp <- dp * m[i, j]
            fimse
            se ((i + j) = (lsup + 1)) entao
                ds <- ds * m[i, j]
            fimse
        fimpara
    fimpara
    
    det <- dp - ds
    
    escreval
    escreval("Matriz:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("O seu determinante é", det,".")
Fimalgoritmo
