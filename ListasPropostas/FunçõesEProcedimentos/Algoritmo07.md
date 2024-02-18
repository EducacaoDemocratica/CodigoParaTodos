# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - FuncaoProcedimento"
funcao menu(): inteiro
Var
    opcao: inteiro
Inicio
    escreval
    escreval("FUNÇÕES DISPONÍVEIS:")
    escreval
    escreval("0 - SAIR")
    escreval("1 - ENFILEIRAR")
    escreval("2 - DESENFILEIRAR")
    escreval("3 - MOSTRAR A FILA")
    escreval("4 - VERIFICAR SE A FILA ESTÁ VAZIA")
    escreval("5 - VERIFICAR SE A FILA ESTÁ CHEIA")
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
    f, i, lsup: inteiro
Inicio
    lsup <- 5
    f <- menu()
    enquanto (f <> 0) faca
        se (f = 1) entao
            enfileirar(i, lsup)
        senao
            se (f = 2) entao
                desenfileirar(lsup)
            senao
                se (f = 3) entao
                    mostrarFila(i)
                senao
                    se (f = 4) entao
                        se (estaVazia(lsup) = verdadeiro) entao
                            escreval("A fila está vazia.")
                        senao
                            escreval("A fila não está vazia.")
                        fimse
                    senao
                        se (estaCheia(lsup) = verdadeiro) entao
                            escreval("A fila está cheia.")
                        senao
                            escreval("A fila não está cheia.")
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
    escreva("Insira um elemento à fila: ")
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

procedimento enfileirar(Var i: inteiro; lsup: inteiro)
Var
Inicio
    se (estaCheia(lsup) = falso) entao
        i <- i + 1
        filas[i] <- lerPalavra()
        enquanto (estaPresente(i) = verdadeiro) faca
            escreva("Esse elemento já está inserido: ")
            leia(filas[i])
            filas[i] <- lerPalavra()
        fimenquanto
        escreval("Elemento inserido com sucesso!")
    senao
        escreval("A fila está cheia. Remova um elemento!")
    fimse
fimProcedimento

procedimento desenfileirar(lsup: inteiro)
Var
    i: inteiro
Inicio
    se (estaVazia(lsup) = falso) entao
        i <- 1
        escreval("Elemento ", filas[i]," removido com sucesso.")
        enquanto ((i < lsup) e (filas[i] <> "")) faca
            i <- i + 1
            filas[i - 1] <- filas[i]
        fimenquanto
        filas[i] <- ""
    senao
        escreval("A fila está vazia. Adicione um elemento!")
    fimse
fimProcedimento

procedimento mostrarFila(lsup: inteiro)
Var
    i: inteiro
Inicio
    i <- 1
    se (estaVazia(lsup) = falso) entao
        escreval
        escreval("FILA:")
        escreval
        enquanto ((filas[i] <> "") e (i <= lsup)) faca
            escreval(i,"º elemento: ", filas[i])
            i <- i + 1
        fimenquanto
    senao
        escreval("A fila está vazia. Adicione um elemento!")
    fimse
fimProcedimento

funcao estaPresente(i: inteiro): logico
Var
    j: inteiro
    r: logico
Inicio
    r <- falso
    para j de 1 ate i faca
        se ((i <> j) e (filas[i] = filas[j])) entao
            r <- verdadeiro
        fimse
    fimpara
    retorne r
fimFuncao

funcao estaVazia(lsup: inteiro): logico
Var
    i, n: inteiro
Inicio
    n <- 0
    para i de 1 ate lsup faca
        se (filas[i] <> "") entao
            n <- n + 1
        fimse
    fimpara
    se (n = 0) entao
        retorne verdadeiro
    senao
        retorne falso
    fimse
fimFuncao

funcao estaCheia(lsup: inteiro): logico
Var
    i, n: inteiro
Inicio
    n <- 0
    para i de 1 ate lsup faca
        se (filas[i] <> "") entao
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
    filas: vetor [1..20] de caractere
Inicio
    principal()
Fimalgoritmo
