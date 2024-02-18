# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
    cidadeorigem: caractere
    sexo: caractere
    altura: real
    peso: real
    imc: real
fimRegistro

Var
    aluno: vetor [1..40] de TAluno
    i, j, tam, lsup: inteiro
    aux, caract: caractere
    m: real

Inicio
    lsup <- 40
    m <- 0
    
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
        
        escreva("Insira o peso: ")
        leia(aluno[i].peso)
        
        enquanto (aluno[i].peso <= 0) faca
            escreva("Insira um peso maior que 0: ")
            leia(aluno[i].peso)
        fimenquanto
        
        aluno[i].imc <- (aluno[i].peso / (aluno[i].altura ^ 2))
        m <- m + aluno[i].imc
        escreval
    fimpara
    
    m <- m / i
    escreval("IMC médio da turma:", m:6:2,".")
    escreval
    escreval("Alunos com IMC acima da média: ")
    escreval
    
    para i de 1 ate lsup faca
        se (aluno[i].imc > m) entao
            escreval("Nome:", aluno[i].nome,"; IMC:", aluno[i].imc:6:2,".")
        fimse
    fimpara
Fimalgoritmo
