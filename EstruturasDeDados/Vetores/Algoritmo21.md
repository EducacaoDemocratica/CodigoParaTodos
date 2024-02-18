# Exercício 21

[**Ver Análise**](Analise21.md)

```markdown

Algoritmo "Q21 - exVetor"
Var
    i, lsup, maior: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    maior <- 0
    para i de 1 ate lsup faca
        escreva("Insira o ", i, " número: ")
        leia(v[i])
        enquanto (v[i] <= 0) faca
            escreva("Insira um número diferente de 0: ")
            leia(v[i])
        fimenquanto
        se (v[i] > maior) entao
            maior <- v[i]
        fimse
    fimpara
    escreval
    escreval("O maior número inserido no vetor é ", maior, ".")
Fimalgoritmo