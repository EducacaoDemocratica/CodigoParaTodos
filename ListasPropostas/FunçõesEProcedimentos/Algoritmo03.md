# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown
Algoritmo "Q3 - FuncaoProcedimento"
funcao validaCPF(cpf: caractere): logico
Var
    ncpf: vetor [1..11] de inteiro
    s1, s2, i, r1, r2, n: inteiro
    caract: caractere
Inicio
    s1 <- 0
    s2 <- 0
    se (compr(cpf) <> 11) entao
        retorne falso
    senao
        para i de 1 ate 11 faca
            caract <- copia(cpf, i, 1)
            n <- caracpnum(caract)
            ncpf[i] <- n
        fimpara

        n <- 0
        para i de 1 ate 10 faca
            se (ncpf[i] = ncpf[i + 1]) entao
                n <- n + 1
            fimse
        fimpara

        se (n = 10) entao
            retorne falso
        senao
            para i de 1 ate 9 faca
                s1 <- s1 + (ncpf[i] * (11 - i))
            fimpara

            r1 <- s1 mod 11
            se (r1 < 2) entao
                r1 <- 0
            senao
                r1 <- 11 - r1
            fimse

            para i de 1 ate 10 faca
                s2 <- s2 + (ncpf[i] * (12 - i))
            fimpara

            r2 <- s2 mod 11
            se (r2 < 2) entao
                r2 <- 0
            senao
                r2 <- 11 - r2
            fimse

            se ((r1 = ncpf[10]) e (r2 = ncpf[11])) entao
                retorne verdadeiro
            senao
                retorne falso
            fimse
        fimse
    fimse
fimFuncao

funcao somenteDigitos(cpf: caractere): caractere
Var
    tam, i: inteiro
    p, caract: caractere
Inicio
    p <- ""
    tam <- compr(cpf)
    para i de 1 ate tam faca
        caract <- copia(cpf, i, 1)
        se ((asc(caract) >= 48) e (asc(caract) <= 57)) entao
            p <- p + caract
        fimse
    fimpara
    retorne p
fimFuncao

procedimento lerCPF()
Var
    cpf: caractere
Inicio
    escreva("Insira o CPF (somente números): ")
    leia(cpf)
    cpf <- somenteDigitos(cpf)
    escreval
    se (validaCPF(cpf) = falso) entao
        escreva("Esse CPF é inválido.")
    senao
        escreva("Esse CPF é válido.")
    fimse
fimProcedimento

Var
Inicio
    lerCPF()
Fimalgoritmo
