# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown


Algoritmo "Q5 - exMatriz"
Var
i, j, lsup: inteiro
m: vetor [1..3, 1..3] de inteiro
s: vetor [1..3] de inteiro
Inicio
    lsup <- 3
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            m[i, j] <- j + ((i - 1) * 3)
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            s[i] <- s[i] + m[i, j]
        fimpara
    fimpara
    
    escreval("Elementos da matriz: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    
    escreval
    
    para i de 1 ate lsup faca
        escreval("Soma dos elementos da", i,"ª coluna: ", s[i],".")
    fimpara
Fimalgoritmo
