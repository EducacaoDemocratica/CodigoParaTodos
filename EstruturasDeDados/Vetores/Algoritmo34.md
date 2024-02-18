# Exercício 34

[**Ver Análise**](Analise34.md)

```markdown
Algoritmo "Q34 - exVetor"
Var
    i, lsup: inteiro
    x, y: vetor [1..20] de inteiro
    p: real

Inicio
    lsup <- 5
    p <- 0

    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número do vetor x: ")
        leia(x[i])
    fimpara
    
    escreval
    
    para i de 1 ate lsup faca
        escreva("Insira o", i, "º número do vetor y: ")
        leia(y[i])
    fimpara
    
    escreval
    
    para i de 1 ate lsup faca
        p <- p + x[i] * y[i]
    fimpara
    
    escreva("Vetor x:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(x[i], ".")
        senao
            escreva(x[i], ",")
        fimse
    fimpara
    
    escreva("Vetor y:")
    para i de 1 ate lsup faca
        se (i = lsup) entao
            escreval(y[i], ".")
        senao
            escreva(y[i], ",")
        fimse
    fimpara
    
    escreval("Produto escalar entre x e y:", p)
Fimalgoritmo

