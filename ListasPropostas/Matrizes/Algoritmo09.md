# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown
Algoritmo "Q9 - Matriz"
Var
    a, b, h: vetor [1..6, 1..6] de inteiro
    vaux: vetor [1..36] de inteiro
    i, j, k, c, d, f, g, p, aux: inteiro
Inicio
    escreva("Insira a quantidade de linhas da matriz A: ")
    leia(c)
    enquanto ((c < 1) ou (c > 6)) faca
        escreva("Insira valores de 1 a 6: ")
        leia(c)
    fimenquanto
    
    escreva("Insira a quantidade de colunas da matriz A: ")
    leia(d)
    enquanto ((d < 1) ou (d > 6)) faca
        escreva("Insira valores de 1 a 6: ")
        leia(d)
    fimenquanto
    
    escreval
    escreva("Insira a quantidade de linhas da matriz B: ")
    leia(f)
    enquanto ((f < 1) ou (f > 6)) faca
        escreva("Insira valores de 1 a 6: ")
        leia(f)
    fimenquanto
    
    escreva("Insira a quantidade de colunas da matriz B: ")
    leia(g)
    enquanto ((g < 1) ou (g > 6)) faca
        escreva("Insira valores de 1 a 6: ")
        leia(g)
    fimenquanto
    
    escreval
    para i de 1 ate c faca
        para j de 1 ate d faca
            p <- j + ((i - 1) * c)
            escreva("Insira o", p,"º valor da matriz A: ")
            leia(a[i, j])
        fimpara
    fimpara
    
    escreval
    para i de 1 ate f faca
        para j de 1 ate g faca
            p <- j + ((i - 1) * f)
            escreva("Insira o", p,"º valor da matriz B: ")
            leia(b[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("Matriz A:")
    escreval
    para i de 1 ate c faca
        para j de 1 ate d faca
            escreva(a[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    escreval("Matriz B:")
    escreval
    para i de 1 ate f faca
        para j de 1 ate g faca
            escreva(b[i, j])
        fimpara
        escreval
    fimpara
    
    escreval
    se (d <> f) entao
        escreval("Não é possível realizar o produto matricial entre A e B.")
    senao
        p <- 0
        para i de 1 ate c faca
            para j de 1 ate g faca
                aux <- 0
                para k de 1 ate c faca
                    aux <- aux + (a[i, k] * b[k, j])
                fimpara
                p <- p + 1
                vaux[p] <- aux
            fimpara
        fimpara
        
        p <- 0
        para i de 1 ate c faca
            para j de 1 ate g faca
                p <- p + 1
                h[i, j] <- vaux[p]
            fimpara
        fimpara
        
        escreval("Matriz H/produto: ")
        escreval
        para i de 1 ate c faca
            para j de 1 ate g faca
                escreva(h[i, j])
            fimpara
            escreval
        fimpara
    fimse
Fimalgoritmo
