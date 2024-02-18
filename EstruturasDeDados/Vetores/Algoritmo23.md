# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown

Algoritmo "Q23 - exVetor"
Var
    i, lsup, x, y: inteiro
    v: vetor [1..20] de inteiro
Inicio
    lsup <- 20
    para i de 1 ate lsup faca
        escreva("Insira o ", i, "º número: ")
        leia(v[i])
    fimpara
    escreval
    escreva("Insira o valor de x: ")
    leia(x)
    enquanto ((x <= 0) ou (x > lsup)) faca
        escreva("Insira um número maior que 0 e menor/igual a 20: ")
        leia(x)
    fimenquanto
    escreva("Insira o valor de y: ")
    leia(y)
    enquanto (((y <= 0) ou (y > lsup)) ou (x = y)) faca
        se (x = y) entao
            escreva("x e y devem ser diferentes: ")
        senao
            escreva("Insira um número maior que 0 e menor/igual a 20: ")
        fimse
        leia(y)
    fimenquanto
    escreval("A soma do valor na ", x, "ª posição com a ", y, "ª posição é: ", v[x] + v[y])
Fimalgoritmo