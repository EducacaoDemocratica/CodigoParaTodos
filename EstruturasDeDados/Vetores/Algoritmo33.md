# Exercício 33

[**Ver Análise**](Analise33.md)

```markdown

Algoritmo "Q33 - exVetor"
Var
    i, lsup, aux, d: inteiro
    v: vetor [1..10] de inteiro
    existe: logico
Inicio
    lsup <- 10
    existe <- falso
    
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
        aux <- 0
        d <- 0
        
        enquanto (aux < v[i]) faca
            aux <- aux + 1
            se (v[i] mod aux = 0) entao
                d <- d + 1
            fimse
        fimenquanto
        
        se (d = 2) entao
            existe <- verdadeiro
        fimse
    fimpara
    
    se (existe = falso) entao
        escreval("Não existem números primos nesse vetor.")
    senao
        escreval("Elementos que são primos:")
        escreval
        
        para i de 1 ate lsup faca
            aux <- 0
            d <- 0
            
            enquanto (aux < v[i]) faca
                aux <- aux + 1
                se (v[i] mod aux = 0) entao
                    d <- d + 1
                fimse
            fimenquanto
            
            se (d = 2) entao
                escreval(v[i], " na ", i, "ª posição.")
            fimse
        fimpara
    fimse
Fimalgoritmo
