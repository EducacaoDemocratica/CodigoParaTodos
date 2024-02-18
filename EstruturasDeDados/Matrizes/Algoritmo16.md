# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown
Algoritmo "Q16 - exMatriz"
Var
    i, j, lsupl, lsupc, n: inteiro
    m: vetor [1..3, 1..4] de inteiro
    menor: vetor [1..3] de inteiro
Inicio
    lsupl <- 3
    lsupc <- 4
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            se (j = 1) entao
                menor[i] <- m[i, j]
            senao
                se (m[i, j] < menor[i]) entao
                    menor[i] <- m[i, j]
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
    para i de 1 ate lsupl faca
        escreval("Menor valor da",i,"ª linha:", menor[i],".")
    fimpara
Fimalgoritmo


