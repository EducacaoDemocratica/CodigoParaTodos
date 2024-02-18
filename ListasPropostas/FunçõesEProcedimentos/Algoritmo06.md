# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - FuncaoProcedimento"
funcao lerLinha(): inteiro
Var
Inicio
    escreval
    escreva("Insira uma linha: ")
    leia(l)
    enquanto ((l < linf) ou (l > lsup) ou (l < (latual - 1)) ou (l > (latual + 1))) faca
        escreva("Valor fora da vizinha ou além do tabuleiro. Insira outra linha: ")
        leia(l)
    fimenquanto
    retorne l
fimFuncao

funcao lerColuna(): inteiro
Var
Inicio
    escreva("Insira uma coluna: ")
    leia(c)
    enquanto ((c < linf) ou (c > lsup) ou (c < (catual - 1)) ou (c > (catual + 1))) faca
        escreva("Valor fora da vizinha ou além do tabuleiro. Insira outra coluna: ")
        leia(c)
    fimenquanto
    retorne c
fimFuncao

procedimento imprimirMatriz()
Var
    i, j: inteiro
Inicio
    escreval
    escreval
    escreval("1 2 3 4 5 6 7 8")
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            se (j = 1) entao
                escreva(i," ")
            fimse
            escreva(m[i, j]," ")
        fimpara
        escreval
    fimpara
fimProcedimento

procedimento preencherMatriz()
Var
    i, j: inteiro
Inicio
    para i de 1 ate lsup faca
        para j de 1 ate lsup faca
            m[i, j] <- "*"
        fimpara
    fimpara
    cinicio <- randi(7) + 1
    m[lsup, cinicio] <- "J"
    latual <- lsup
    catual <- cinicio
fimProcedimento

procedimento gerarBombas()
Var
    n, i, l, c: inteiro
Inicio
    i <- 0
    escreva("Insira a quantidade de bombas: ")
    leia(n)
    enquanto ((n < 5) ou (n > 20)) faca
        escreva("Escolha de 5 a 20 bombas: ")
        leia(n)
    fimenquanto
    enquanto (i < n) faca
        l <- randi(7) + 1
        c <- randi(7) + 1
        se ((mb[l, c] = "") e ((c <> catual) e (l <> latual))) entao
            i <- i + 1
            mb[l, c] <- "BOMBA"
        fimse
    fimenquanto
fimProcedimento

funcao contarBombas(): inteiro
Var
    n, i, j, lsupLinha, linfLinha, lsupColuna, linfColuna: inteiro
Inicio
    se (latual = linf) entao
        linfLinha <- latual
        lsupLinha <- latual + 1
    senao
        se (latual = lsup) entao
            linfLinha <- latual - 1
            lsupLinha <- latual
        senao
            linfLinha <- latual - 1
            lsupLinha <- latual + 1
        fimse
    fimse
    se (catual = linf) entao
        linfColuna <- catual
        lsupColuna <- catual + 1
    senao
        se (catual = lsup) entao
            linfColuna <- catual - 1
            lsupColuna <- catual
        senao
            linfColuna <- catual - 1
            lsupColuna <- catual + 1
        fimse
    fimse
    para i de linfLinha ate lsupLinha faca
        para j de linfColuna ate lsupColuna faca
            se (mb[i, j] = "BOMBA") entao
                n <- n + 1
            fimse
        fimpara
    fimpara
    retorne n
fimFuncao

procedimento calcular()
Var
Inicio
    se (mb[l, c] = "BOMBA") entao
        escreval
        escreval("BOMBA DESARMADA!")
        escreval
        mb[l, c] <- "DESARMADA"
        m[latual, catual] <- "X"
        m[l, c] <- "B"
        latual <- lsup
        catual <- cinicio
        m[latual, catual] <- "J"
    senao
        m[latual, catual] <- "X"
        m[l, c] <- "J"
        latual <- l
        catual <- c
    fimse
fimProcedimento

Var
    m, mb: vetor [1..8, 1..8] de caractere
    l, latual, catual, c, linf, lsup, cinicio, jogadas: inteiro
Inicio
    linf <- 1
    lsup <- 8
    jogadas <- 0
    preencherMatriz()
    gerarBombas()
    enquanto (l <> 1) faca
        imprimirMatriz()
        escreval
        escreval("Existem", contarBombas()," bombas ao seu redor.")
        l <- lerLinha()
        c <- lerColuna()
        enquanto ((l = latual) e (c = catual)) faca
            l <- lerLinha()
            c <- lerColuna()
        fimenquanto
        calcular()
        jogadas <- jogadas + 1
    fimenquanto
    imprimirMatriz()
    escreval()
    escreval("O jogador fez", jogadas, " movimentos.")
Fimalgoritmo
