# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - Matriz"
Var
    m: vetor [1..3, 1..3] de inteiro
    i, j, k, p, lsup, dp, ds, det, aux: inteiro
Inicio
    det <- 0
    lsup <- 3
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * 3)
            escreva("Insira o", p,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    para k de 1 ate lsup faca
        p <- 0
        ds <- 1
        dp <- 1
        para i de 2 ate lsup faca
            para j de 1 ate lsup faca
                se (j <> k) entao
                    p <- p + 1
                    se ((p = 1) ou (p = 4)) entao
                        dp <- dp * m[i, j]
                    senao
                        ds <- ds * m[i, j]
                    fimse
                fimse
            fimpara
        fimpara
        aux <- dp - ds
        aux <- aux * m[1, k]
        se (k mod 2 = 0) entao
            det <- det - aux
        senao
            det <- det + aux
        fimse
    fimpara
    
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
