# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
fimRegistro

Var
    aluno: vetor [1..40] de TAluno
    i, j, tam, lsup, maior: inteiro
    aux, caract: caractere

Inicio
    lsup <- 5
    
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
            maior <- aluno[i].idade
        senao
            se (maior < aluno[i].idade) entao
                maior <- aluno[i].idade
            fimse
        fimse
        
        escreval
    fimpara
    
    escreval("A maior idade da turma é a de", maior," anos.")
Fimalgoritmo
