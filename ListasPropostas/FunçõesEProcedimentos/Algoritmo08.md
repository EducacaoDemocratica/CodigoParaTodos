# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - FuncaoProcedimento"

funcao menu(): inteiro
    Var
        opcao: inteiro
    Inicio
        escreval
        escreval("FUNÇÕES DISPONÍVEIS:")
        escreval
        escreval("0 - SAIR")
        escreval("1 - EMPILHAR/PUSH")
        escreval("2 - DESEMPILHAR/POP")
        escreval("3 - MOSTRAR O TOPO")
        escreval("4 - VERIFICAR SE A PILHA ESTÁ VAZIA")
        escreval("5 - VERIFICAR SE A PILHA ESTÁ CHEIA")
        escreval
        escreva("Selecione uma opção: ")
        leia (opcao)
        enquanto ((opcao < 0) ou (opcao > 5)) faca
            escreva("Selecione um número de 0 a 5: ")
            leia (opcao)
        fimenquanto
        retorne opcao
    fimFuncao

procedimento principal()
    Var
        f, i, topo, lsup: inteiro
    Inicio
        lsup <- 20
        f <- menu()
        enquanto (f <> 0) faca
            se (f = 1) entao
                empilhar(topo, lsup)
            senao
                se (f = 2) entao
                    desempilhar(topo, lsup)
                senao
                    se (f = 3) entao
                        mostrarTopo(topo, lsup)
                    senao
                        se (f = 4) entao
                            se (estaVazia(topo, lsup) = verdadeiro) entao
                                escreval("A pilha está vazia.")
                            senao
                                escreval("A pilha não está vazia.")
                            fimse
                        senao
                            se (estaCheia(topo, lsup) = verdadeiro) entao
                                escreval("A pilha está cheia.")
                            senao
                                escreval("A pilha não está cheia.")
                            fimse
                        fimse
                    fimse
                fimse
            fimse
            f <- menu()
        fimenquanto
    fimProcedimento

funcao lerPalavra(): caractere
    Var
        palavra, caract, nome: caractere
        i: inteiro
    Inicio
        escreva("Insira um elemento à pilha: ")
        leia(nome)
        nome <- maiusc(nome)
        palavra <- ""
        para i de 1 ate compr(nome) faca
            caract <- copia(nome; i; 1)
            se (caract <> " ") entao
                palavra <- palavra + caract
            fimse
        fimpara
        se (palavra = "") entao
            nome <- lerPalavra()
        fimse
        retorne palavra
    fimFuncao

procedimento empilhar(Var topo, lsup: inteiro)
    Var
    Inicio
        se (estaCheia(topo, lsup) = falso) entao
            topo <- topo + 1
            pilha[topo] <- lerPalavra()
            enquanto (estaPresente(topo) = verdadeiro) faca
                escreva("Esse elemento já está inserido: ")
                pilha[topo] <- lerPalavra()
            fimenquanto
            escreval("Elemento inserido com sucesso!")
        senao
            escreval("A pilha está cheia. Remova um elemento!")
        fimse
    fimProcedimento

procedimento desempilhar(Var topo: inteiro; lsup: inteiro)
    Var
    Inicio
        se (estaVazia(topo, lsup) = falso) entao
            escreval("Elemento ", pilha[topo]," removido com sucesso.")
            pilha[topo] <- ""
            topo <- topo - 1
        senao
            escreval("A pilha está vazia. Adicione um elemento!")
        fimse
    fimProcedimento

procedimento mostrarTopo(topo, lsup: inteiro)
    Var
    Inicio
        se (estaVazia(topo, lsup) = falso) entao
            escreval("Topo da fila:", topo,"° elemento - ", pilha[topo])
        senao
            escreval("A pilha está vazia. Adicione um elemento!")
        fimse
    fimProcedimento

funcao estaPresente(i: inteiro): logico
    Var
        j: inteiro
        r: logico
    Inicio
        r <- falso
        para j de 1 ate i faca
            se ((i <> j) e (pilha[i] = pilha[j])) entao
                r <- verdadeiro
            fimse
        fimpara
        retorne r
    fimFuncao

funcao estaVazia(topo, lsup: inteiro): logico
    Var
        i, n: inteiro
    Inicio
        n <- 0
        para i de 1 ate lsup faca
            se (pilha[i] <> "") entao
                n <- n + 1
            fimse
        fimpara
        se (n = 0) entao
            retorne verdadeiro
        senao
            retorne falso
        fimse
    fimFuncao

funcao estaCheia(topo, lsup: inteiro): logico
    Var
        i, n: inteiro
    Inicio
        n <- 0
        para i de 1 ate lsup faca
            se (pilha[i] <> "") entao
                n <- n + 1
            fimse
        fimpara
        se (n = lsup) entao
            retorne verdadeiro
        senao
            retorne falso
        fimse
    fimFuncao

Var
    pilha: vetor [1..20] de caractere
Inicio
    principal()
Fimalgoritmo
