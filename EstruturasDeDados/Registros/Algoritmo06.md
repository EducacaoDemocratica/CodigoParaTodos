# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
fimRegistro

Var
    aluno: vetor [1..40] de TAluno
    n: vetor [1..40] de inteiro
    i, j, tam, lsup, menor, q: inteiro
    aux, caract: caractere

Inicio
    lsup <- 40
    q <- 1
    
    para i de 1 ate lsup faca
        escreva("Insira o nome do",i,"º aluno: ")
        leia(aluno[i].nome)
        aux <- ""
        tam <- compr(aluno[i].nome)
        
        para j de 1 ate tam faca
            caract <- copia(aluno[i].nome; j; 1)
            se (caract <> " ") entao
                aux <- aux + caract
            fimse
        fimpara
        
        enquanto (aux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(aluno[i].nome)
            aux <- ""
            tam <- compr(aluno[i].nome)
            
            para j de 1 ate tam faca
                caract <- copia(aluno[i].nome; j; 1)
                se (caract <> " ") entao
                    aux <- aux + caract
                fimse
            fimpara
        fimenquanto
        
        escreva("Insira a idade do", i,"º aluno: ")
        leia(aluno[i].idade)
        
        enquanto (aluno[i].idade <= 0) faca
            escreva("Insira uma idade maior que 0: ")
            leia(aluno[i].idade)
        fimenquanto
        
        se (i = 1) entao
            menor <- aluno[i].idade
            n[q] <- 1
        senao
            se (menor > aluno[i].idade) entao
                menor <- aluno[i].idade
                para j de 1 ate lsup faca
                    n[j] <- 0
                fimpara
                q <- 1
                n[q] <- i
            senao
                se (menor = aluno[i].idade) entao
                    q <- q + 1
                    n[q] <- i
                fimse
            fimse
        fimse
        
        escreval
    fimpara
    
    escreva("A menor idade da turma é a de", menor," anos e ")
    para i de 1 ate q faca
        se (i = q) entao
            escreval(aluno[n[i]].nome," a possui(em).")
        senao
            escreva(aluno[n[i]].nome,", ")
        fimse
    fimpara
Fimalgoritmo
