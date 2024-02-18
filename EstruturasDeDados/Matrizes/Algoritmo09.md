# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown


Algoritmo "Q9 - Matriz"
Var
    i, j, lsupl, lsupc: inteiro
    m: vetor [1..4, 1..2] de real
Inicio
    lsupl <- 4
    lsupc <- 2
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva("Insira o", j + ((i - 1) * 3 ),"º valor da matriz: ")
            leia(m[i, j])
            enquanto ((m[i, j] <= -6) ou (m[i, j] > 3)) faca
                escreva("Os valores devem pertencer ao intervalo ]-6, 3]: ")
                leia(m[i, j])
            fimenquanto
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
Fimalgoritmo
