# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown

Algoritmo "Q15 - exMatriz"
Var
    i, j, lsupl, lsupc, n, maior: inteiro
    m: vetor [1..3, 1..4] de inteiro
Inicio
    lsupl <- 3
    lsupc <- 4
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            se ((i = 1) e (j = 1)) entao
                maior <- m[i, j]
            senao
                se (m[i, j] > maior) entao
                    maior <- m[i, j]
                fimse
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
    escreval("O maior valor da estrutura é:", maior,".")
Fimalgoritmo

