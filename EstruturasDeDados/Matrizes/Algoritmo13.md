# Exercício 13

[**Ver Análise**](Analise13.md)

```markdown

Algoritmo "Q13 - exMatriz"
Var
    i, j, lsup, n: inteiro
    m: vetor [1..5, 1..5] de inteiro
    s, media: real
Inicio
    lsup <- 5
    s <- 0
    i <- 1
    enquanto (i <= lsup) faca
        j <- 1
        enquanto (j <= lsup) faca
            n <- j + ((i - 1) * 5)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
            se (m[i, j] <= 0) entao
                m[i, j] <- 0
                n <- n - 1
            senao
                s <- s + m[i, j]
            fimse
            j <- j + 1
        fimenquanto
        i <- i + 1
    fimenquanto
    se (n = 0) entao
        escreval("Nenhum valor foi inserido na matriz!")
    senao
        escreval
        escreval("Elementos da matriz: ")
        escreval
        para i de 1 ate lsup faca
            para j de 1 ate lsup faca
                se (m[i, j] <> 0) entao
                    escreva(m[i, j]," ")
                se (j mod 5 = 0) entao
                    escreval
                fimse
            fimpara
        fimpara
        escreval
        escreval
        media <- s/n
        escreval("Média dos valores inseridos na estrutura:", media:6:2,".")
    fimse
Fimalgoritmo

