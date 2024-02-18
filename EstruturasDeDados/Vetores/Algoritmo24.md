# Exercício 24

[**Ver Análise**](Analise24.md)

```markdown

Algoritmo "Q24 - exVetor"
Var
    i, imaior, imenor, menor, maior, lsup: inteiro
    v: vetor [1..100] de inteiro
Inicio
    lsup <- 100
    para i de 1 ate lsup faca
        escreva("Insira o ", i, "º número: ")
        leia(v[i])
        se (i = 1) entao
            menor <- v[i]
            imenor <- i
            maior <- v[i]
            imaior <- i
        senao
            se (v[i] < menor) entao
                menor <- v[i]
                imenor <- i
            fimse
            se (v[i] > maior) entao
                maior <- v[i]
                imaior <- i
            fimse
        fimse
    fimpara
    escreval
    escreval("O maior número é ", maior, " e está na ", imaior, "ª posição.")
    escreval("O menor número é ", menor, " e está na ", imenor, "ª posição.")
Fimalgoritmo