# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - FuncaoProcedimento"
funcao fatorial(n: inteiro): real
Var
    i: inteiro
    f: real
Inicio
    i <- 0
    f <- 1
    enquanto (i < n) faca
        i <- i + 1
        f <- f * i
    fimenquanto
    retorne f
fimFuncao

funcao verificarPalavra(palavra: caractere): caractere
Var
    p, caract: caractere
    i: inteiro
Inicio
    p <- ""
    palavra <- maiusc(palavra)
    i <- 1
    faca
        enquanto ((copia(palavra, i, 1) <> " ") e (compr(palavra) >= i))
            caract <- copia(palavra; i; 1)
            se ((asc(caract) >= 65) e (asc(caract) <= 90)) entao
                p <- p + caract
            fimse
            i <- i + 1
        fimenquanto
        retorne p
    fimFuncao

procedimento contarRepeticoes(palavra: caractere)
Var
    v: vetor [1..46] de caractere
    vaux: vetor [1..26] de caractere
    k, i, j, lsup, achou: inteiro
Inicio
    lsup <- compr(palavra)
    para i de 1 ate lsup faca
        v[i] <- copia(palavra, i, 1)
    fimpara
    k <- 0
    para i de 1 ate lsup faca
        achou <- 1
        para j de 1 ate lsup faca
            se (vaux[j] = v[i]) entao
                r[j] <- r[j] + 1
                achou <- 0
            fimse
        fimpara
        se (achou = 1) entao
            k <- k + 1
            vaux[k] <- v[i]
            r[k] <- 1
        fimse
    fimpara
fimProcedimento

procedimento imprimir(palavra: caractere)
Var
    tam, i, j, c, aux, lsup: inteiro
    den: real
Inicio
    den <- 1
    c <- 0
    permutacoes <- fatorial(compr(palavra))
    escreval
    escreva("Permutações(", palavra, "): ")
    lsup <- 26
    para i de 1 ate lsup faca
        den <- den * fatorial(r[i])
        se (r[i] > 1) entao
            c <- c + 1
            aux <- 0
            para j de (i + 1) ate lsup faca
                se (r[j] > 1) entao
                    aux <- 1
                fimse
            fimpara
            se (aux = 1) entao
                escreva(r[i], "! X ")
            senao
                escreva(r[i], "!")
            fimse
        fimse
    fimpara
    permutacoes <- permutacoes / den
    se (c = 0) entao
        escreva(" 1")
    fimse
    escreval()
    escreval("Um total de ", permutacoes, " resultados.")
Fimalgoritmo

Var
    palavra: caractere
    r: vetor [1..26] de inteiro
    permutacoes: real
Inicio
    escreva("Insira uma única palavra de até 46 caracteres: ")
    leia(palavra)
    palavra <- verificarPalavra(palavra)
    enquanto ((palavra = "") ou (compr(palavra) > 46)) faca
        se (compr(palavra) > 46) entao
            escreva("Insira até 46 caracteres: ")
        senao
            escreva("Não preencha com espaços vazios: ")
        fimse
        leia(palavra)
        palavra <- verificarPalavra(palavra)
    fimenquanto
    contarRepeticoes(palavra)
    imprimir(palavra)
Fimalgoritmo
