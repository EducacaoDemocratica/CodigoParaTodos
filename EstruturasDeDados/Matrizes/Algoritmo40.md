# Exercício 40

[**Ver Análise**](Analise40.md)

```markdown 
Algoritmo "Q40 - exMatriz"
Var
    i, j, n, lsup, aux: inteiro
    m: vetor [1..10, 1..10] de inteiro
Inicio
    lsup <- 10
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 10)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("Matriz original: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    para j de 1 ate lsup faca
        aux <- m[8, j]
        m[8, j] <- m[2, j]
        m[2, j] <- aux
    fimpara
    
    escreval
    escreval("Após troca da segunda linha pela oitava linha: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    para i de 1 ate lsup faca
        aux <- m[i, 4]
        m[i, 4] <- m[i, 10]
        m[i, 10] <- aux
    fimpara
    
    escreval
    escreval("Após troca da quarta coluna pela décima coluna: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) = (lsup + 1)) entao
                aux <- m[i, i]
                m[i, i] <- m[i, j]
                m[i, j] <- aux
            fimse
        fimpara
    fimpara
    
    escreval
    escreval("Após troca das diagonais: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j], " ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
