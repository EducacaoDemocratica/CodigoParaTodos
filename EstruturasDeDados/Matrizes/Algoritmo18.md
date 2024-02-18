# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown
Algoritmo "Q18 - exMatriz"
Var
    i, j, lsupl, lsupc, n, maior, menor, jmaior: inteiro
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
                jmaior <- j
            senao
                se (m[i, j] > maior) entao
                    maior <- m[i, j]
                    jmaior <- j
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
        se (i = 1) entao
            menor <- m[i, jmaior]
        senao
            se (m[i, jmaior] < menor) entao
                menor <- m[i, jmaior]
            fimse
        fimse
    fimpara
    escreval("O maior valor da matriz é", maior," e se encontra na",
        jmaior,"ª coluna.")
    escreval("O menor valor dessa coluna é", menor,".")
Fimalgoritmo
