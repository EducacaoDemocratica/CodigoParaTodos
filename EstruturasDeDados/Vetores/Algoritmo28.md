# Exercício 28

[**Ver Análise**](Analise28.md)

```markdown

Algoritmo "Q29 - exVetor"
Var
    i, lsup, sp, si: inteiro
    v: vetor [1..10] de inteiro
Inicio
    lsup <- 10
    sp <- 0
    si <- 0

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
        se (i mod 2 = 0) entao
            sp <- sp + v[i]
        senao
            si <- si + v[i]
        fimse
    fimpara

    escreval("Soma dos valores nas posições pares: ", sp)
    escreval("Soma dos valores nas posições ímpares: ", si)
    escreval("Diferença: ", sp - si)
Fimalgoritmo
