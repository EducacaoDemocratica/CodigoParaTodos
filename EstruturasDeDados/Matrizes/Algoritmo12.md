# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown

Algoritmo "Q12 - exMatriz"
Var
    i, j, lsupl, lsupc, lsup, n: inteiro
    m: vetor [1..4, 1..6] de inteiro
    s: real
Inicio
    lsupl <- 4
    lsupc <- 6
    s <- 0
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 6)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            se (m[i, j] mod 2 = 0) entao
                s <- s + m[i, j]
            fimse
        fimpara
    fimpara
    escreval
    escreval("Elementos da matriz: ")
    escreval
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    escreval
    escreval("Soma dos números pares da estrutura:", s,".")
Fimalgoritmo

