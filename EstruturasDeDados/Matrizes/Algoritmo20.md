# Exercício 20

[**Ver Análise**](Analise20.md)

```markdown
Algoritmo "Q20 - exMatriz"
Var
    i, j, n, k, aux, lsup: inteiro
    m: vetor [1..4, 1..4] de inteiro
Inicio
    lsup <- 4
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            n <- j + ((i - 1) * 4)
            escreva("Insira o", n,"º valor da matriz: ")
            leia(m[i, j])
        fimpara
    fimpara
    
    escreval
    escreval("Matriz antes da ordenação: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
    
    escreval
    
    para j de 1 ate lsup faca
        para k de (lsup - 1) ate 1 passo -1 faca
            para i de 1 ate k faca
                se (m[i, j] > m[i + 1, j]) entao
                    aux <- m[i, j]
                    m[i, j] <- m[i + 1, j]
                    m[i + 1, j] <- aux
                fimse
            fimpara
        fimpara
    fimpara
    
    escreval("Matriz após a ordenação das colunas: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
