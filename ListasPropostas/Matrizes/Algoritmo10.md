# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown
Algoritmo "Q10 - Matriz"
Var
    a, b, c, d, f: vetor [1..6, 1..6] de inteiro
    i, j, k, p, lsup, aux: inteiro
Inicio
    lsup <- 4
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * lsup)
            escreva("Insira o", p,"º valor da matriz A: ")
            leia(a[i, j])
        fimpara
    fimpara
    
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * lsup)
            escreva("Insira o", p,"º valor da matriz B: ")
            leia(b[i, j])
        fimpara
    fimpara
    
    p <- 0
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            c[i, j] <- a[i, j] + b[i, j]
            d[i, j] <- b[i, j] - a[i, j]
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            aux <- 0
            para k de 1 ate lsup faca
                aux <- aux + (a[i, k] * b[k, j])
            fimpara
            f[i, j] <- aux
        fimpara
    fimpara
    
    escreval
    escreval("Matriz A:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(a[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz B:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(b[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz C:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(c[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz D:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(d[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz F: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(f[i, j])
        fimpara
        escreval
    fimpara
Fimalgoritmo
