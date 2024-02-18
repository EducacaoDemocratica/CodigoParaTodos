# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown


Algoritmo "Q15 - exVetor"
Var
    i, lsup: inteiro
    s: real
    v: vetor [1..70] de inteiro
Inicio
    lsup <- 70
    s <- 0
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número: ")
        leia(v[i])
    fimpara
    escreval
    para i de 1 ate lsup faca
        s <- s + v[i]
    fimpara
    escreval("Soma:", s)
Fimalgoritmo
