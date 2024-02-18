# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown


Algoritmo "Q10 - exMatriz"
Var
    i, j, lsup, n: inteiro
    m: vetor [1..6, 1..6] de inteiro
    v: vetor [1..36] de inteiro
Inicio
    lsup <- 6
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 6)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            v[n] <- m[i, j]
        fimpara
    fimpara
    escreval
    escreval("Elementos da matriz: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    lsup <- lsup * lsup
    escreval
    escreva("Elementos do vetor: ")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i],".")
        senao
            escreva(v[i],",")
        fimse
    fimpara
Fimalgoritmo
