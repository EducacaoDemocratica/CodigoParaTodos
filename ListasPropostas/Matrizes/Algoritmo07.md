# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - Matriz"
Var
    m, mt: vetor [1..5, 1..5] de inteiro
    i, j, p, lsup: inteiro
Inicio
    lsup <- 5
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * 5)
            escreva("Insira o", p,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            mt[i, j] <- m[j, i]
        fimpara
    fimpara
    
    escreval
    escreval("Matriz original:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j])
        fimpara
    escreval
    fimpara
    
    escreval
    escreval("Matriz transposta:")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(mt[i, j])
        fimpara
    escreval
    fimpara
Fimalgoritmo
