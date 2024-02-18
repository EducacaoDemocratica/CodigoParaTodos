# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - Matriz"
Var
    m: vetor [1..3, 1..3] de inteiro
    i, j, k, p, lsup, aux, det: inteiro
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
    
    k <- 1
    para i de 1 ate lsup faca
        k <- k - 1
        aux <- 1
        para j de 1 ate lsup faca
            k <- k + 1
            se (k > lsup) entao
                k <- k - lsup
            fimse
            aux <- aux * m[j, k]
        fimpara
        det <- det + aux
    fimpara
    
    k <- 2
    para i de 1 ate lsup faca
        k <- k + 1
        aux <- 1
        para j de 1 ate lsup faca
            k <- k - 1
            se (k = 0) entao
                k <- lsup
            fimse
            aux <- aux * m[j, k]
        fimpara
        det <- det - aux
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
