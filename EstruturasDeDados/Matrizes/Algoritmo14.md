# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown


Algoritmo "Q14 - exMatriz"
Var
    i, j, lsupl, lsupc, n: inteiro
    m: vetor [1..3, 1..4] de inteiro
    presente: logico
Inicio
    lsupl <- 3
    lsupc <- 4
    presente <- falso
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    escreval
    escreval("Elementos da matriz: ")
    escreval
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    escreval
    escreva("Insira um número inteiro: ")
    leia(n)
    para i de 1 ate lsupl faca
        para j de 1 ate lsupc faca
            se (m[i, j] = n) entao
                presente <- verdadeiro
            fimse
        fimpara
    fimpara
    se (presente = verdadeiro) entao
        escreval(n," está presente na matriz.")
    senao
        escreval(n," não está presente na matriz.")
    fimse
Fimalgoritmo
