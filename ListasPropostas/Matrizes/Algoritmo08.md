# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - Matriz"
Var
    m, mt: vetor [1..5, 1..5] de inteiro
    i, j, p, lsup: inteiro
    simetrica: logico
Inicio
    simetrica <- verdadeiro
    lsup <- 5
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            p <- j + ((i - 1) * 10)
            escreva("Insira o", p,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            mt[i, j] <- m[j, i]
            se (mt[i, j] <> m[i, j]) entao
                simetrica <- falso
            fimse
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
    
    escreval
    se (simetrica = verdadeiro) entao
        escreval("A matriz é simétrica.")
    senao
        escreval("A matriz não é simétrica.")
    fimse
Fimalgoritmo
