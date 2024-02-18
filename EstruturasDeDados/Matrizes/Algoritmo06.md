# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown


Algoritmo "Q6 - exMatriz"
Var
i, j, lsupl, lsupc: inteiro
m: vetor [1..2, 1..4] de inteiro
s: real
Inicio
    lsupl <- 2
    lsupc <- 4
    aleatorio on
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva("Gere o", j + ((i - 1) * 3 ),"º valor da matriz: ")
            leia(m[i, j])
            s <- s + m[i, j]
        fimpara
    fimpara
    aleatorio off
    
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
    escreval("Soma dos elementos da matriz:",s,".")
Fimalgoritmo
