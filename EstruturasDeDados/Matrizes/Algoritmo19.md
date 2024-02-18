# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - exMatriz"
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
    para i de 1 ate lsup faca
        para k de (lsup - 1) ate 1 passo -1 faca
            para j de 1 ate k faca
                se (m[i, j] > m[i, j + 1]) entao
                    aux <- m[i, j]
                    m[i, j] <- m[i, j + 1]
                    m[i, j + 1] <- aux
                fimse
            fimpara
        fimpara
    fimpara
    
    escreval("Matriz após a ordenação das linhas: ")
    escreval
    
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
Fimalgoritmo
