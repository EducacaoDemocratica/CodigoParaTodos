# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown



Algoritmo "Q17 - exVetor"
Var
    i, lsup: inteiro
    v: vetor [1..12] de inteiro
Inicio
    lsup <- 12
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número: ")
        leia(v[i])
        enquanto (v[i] >= 0) faca
            escreva("Insira um número menor que 0: ")
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
