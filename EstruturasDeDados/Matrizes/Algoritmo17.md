# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown
Algoritmo "Q17 - exMatriz"
Var
    i, j, lsupl, lsupc, n, maior, menor, imaior: inteiro
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
                imaior <- i
            senao
                se (m[i, j] > maior) entao
                    maior <- m[i, j]
                    imaior <- i
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
    para j de 1 ate lsupc faca
        se (j = 1) entao
            menor <- m[imaior, j]
        senao
            se (m[imaior, j] < menor) entao
                menor <- m[imaior, j]
            fimse
        fimse
    fimpara
    escreval("O maior valor da matriz é", maior," e se encontra na",
        imaior,"ª linha.")
    escreval("O menor valor dessa linha é", menor,".")
Fimalgoritmo


