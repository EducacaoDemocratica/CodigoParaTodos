# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown

Algoritmo "Q18 - exVetor"
Var
    i, lsup, s: inteiro
    v: vetor [1..10] de inteiro
Inicio
    s <- 0
    lsup <- 10
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º valor do vetor: ")
        leia (v[i])
        enquanto (v[i] <= 0) faca
            escreva("Insira valores maiores que 0: ")
            leia (v[i])
        fimenquanto
    fimpara
    para i de 1 ate lsup faca
        se (v[i] mod 2 = 0) entao
            s <- s + v[i]
        fimse
    fimpara
    escreval
    escreval("A soma dos números pares do vetor é", s, ".")
Fimalgoritmo


