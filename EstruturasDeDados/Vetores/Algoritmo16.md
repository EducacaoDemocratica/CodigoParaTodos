# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown



Algoritmo "Q16 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..15] de inteiro
Inicio
    lsup <- 15
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número: ")
        leia(v[i])
        enquanto (v[i] <= 0) faca
            escreva("Insira um número maior que 0: ")
            leia(v[i])
        fimenquanto
    fimpara
    escreval
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(v[i], ".")
        senao
            escreva(v[i], ",")
        fimse
    fimpara
Fimalgoritmo


