# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown


Algoritmo "Q2 - exMatriz"
Var
    i, j, lsup: inteiro
    m: vetor [1..3, 1..3] de inteiro

Inicio
    lsup <- 3

    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            m[i, j] <- j + ((i - 1) * 3)
        fimpara
    fimpara

    para i de lsup ate 1 passo -1 faca
        para j de lsup ate 1 passo -1 faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara

Fimalgoritmo
