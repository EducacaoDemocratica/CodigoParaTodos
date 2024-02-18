# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown
Algoritmo "Q9 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
    cidadeorigem: caractere
fimRegistro

Var
    aluno: vetor [1..40] de TAluno
    auxAluno: TAluno
    i, j, tam, lsup: inteiro
    aux, caract: caractere

Inicio
    lsup <- 40
    
    para i de 1 ate lsup faca
        escreval("ALUNO", i)
        escreva("Insira o nome: ")
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
        
        escreva("Insira a idade: ")
        leia(aluno[i].idade)
        
        enquanto (aluno[i].idade <= 0) faca
            escreva("Insira uma idade maior que 0: ")
            leia(aluno[i].idade)
        fimenquanto
        
        escreva("Insira a cidade de origem: ")
        leia(aluno[i].cidadeorigem)
        aux <- ""
        tam <- compr(aluno[i].cidadeorigem)
        
        para j de 1 ate tam faca
            caract <- copia(aluno[i].cidadeorigem; j; 1)
            se (caract <> " ") entao
                aux <- aux + caract
            fimse
        fimpara
        
        enquanto (aux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(aluno[i].cidadeorigem)
            aux <- ""
            tam <- compr(aluno[i].cidadeorigem)
            
            para j de 1 ate tam faca
                caract <- copia(aluno[i].cidadeorigem; j; 1)
                se (caract <> " ") entao
                    aux <- aux + caract
                fimse
            fimpara
        fimenquanto
        
        escreval
    fimpara
    
    para j de (lsup - 1) ate 1 passo -1 faca
        para i de 1 ate j faca
            se (maiusc(aluno[i].nome) > maiusc(aluno[i + 1].nome)) entao
                auxAluno <- aluno[i]
                aluno[i] <- aluno[i + 1]
                aluno[i + 1] <- auxAluno
            fimse
        fimpara
    fimpara
    
    para i de 1 ate lsup faca
        escreval("DADOS DO ", i,"º ALUNO:")
        escreval
        escreval("Nome: ", aluno[i].nome,".")
        escreval("Idade:", aluno[i].idade,".")
        escreval("Cidade de origem: ", aluno[i].cidadeorigem,".")
        escreval
    fimpara
Fimalgoritmo
