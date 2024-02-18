# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
    cidadeorigem: caractere
    sexo: caractere
    altura: real
fimRegistro

Var
    aluno: vetor [1..40] de TAluno
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
        
        escreva("Insira o sexo (F - Feminino; M - Masculino): ")
        leia(aluno[i].sexo)
        aluno[i].sexo <- maiusc(aluno[i].sexo)
        
        enquanto ((aluno[i].sexo <> "F") e (aluno[i].sexo <> "M")) faca
            escreva("Insira 'F' ou 'M': ")
            leia(aluno[i].sexo)
            aluno[i].sexo <- maiusc(aluno[i].sexo)
        fimenquanto
        
        se (aluno[i].sexo = "F") entao
            aluno[i].sexo <- "Feminino"
        senao
            aluno[i].sexo <- "Masculino"
        fimse
        
        escreva("Insira a altura: ")
        leia(aluno[i].altura)
        
        enquanto (aluno[i].altura <= 0) faca
            escreva("Insira uma altura maior que 0: ")
            leia(aluno[i].altura)
        fimenquanto
        
        escreval
    fimpara
    
    para i de 1 ate lsup faca
        escreval("DADOS DO ", i,"º ALUNO:")
        escreval
        escreval("Nome: ", aluno[i].nome,".")
        escreval("Idade:", aluno[i].idade,".")
        escreval("Cidade de origem: ", aluno[i].cidadeorigem,".")
        escreval("Sexo: ", aluno[i].sexo,".")
        escreval("Altura:", aluno[i].altura,"m.")
        escreval
    fimpara
Fimalgoritmo
