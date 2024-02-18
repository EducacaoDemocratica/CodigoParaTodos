# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown


Algoritmo "Q8 - exMatriz"
Var
    i, j, lsupl, lsupc: inteiro
    m: vetor [1..8, 1..6] de inteiro
Inicio
    lsupl <- 8
    lsupc <- 6
    aleatorio on
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva("Gere o", j + ((i - 1) * 3 ),"º valor da matriz: ")
            leia(m[i, j])
            enquanto (m[i, j] mod 3 <> 0) faca
                escreva("Gere um múltiplo de 3: ")
                leia(m[i, j])
            fimenquanto
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
Fimalgoritmo
