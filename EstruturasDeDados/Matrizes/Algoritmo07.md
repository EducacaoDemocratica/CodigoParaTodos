# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown


Algoritmo "Q7 - exMatriz"
Var
    i, j, lsup: inteiro
    m: vetor [1..3, 1..3] de inteiro
    s: real
Inicio
    lsup <- 3
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva("Insira o", j + ((i - 1) * 3 ),"º valor da matriz: ")
            leia(m[i, j])
            enquanto (m[i, j] <= 0) faca
                escreva("Insira um valor maior que zero: ")
                leia(m[i, j])
            fimenquanto
            se ((i + j) mod 2 = 0) entao
                s <- s + m[i, j]
            fimse
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
    
    escreval("Elementos em que a soma da coordenada é par: ")
    escreval
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se ((i + j) mod 2 = 0) entao
                escreva(m[i, j]," ")
            senao
                escreva("
")
            fimse
        fimpara
    escreval
    fimpara
    
    escreval("Soma desses elementos da matriz:",s,".")
Fimalgoritmo
