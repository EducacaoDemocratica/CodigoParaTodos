# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown
 Algoritmo "Q11 - exRegistros"

Tipo TFuncionario = registro
    nome: caractere
    sexo: caractere
    idade: inteiro
    salario: real
fimRegistro

Var
    funcionario: vetor [1..30] de TFuncionario
    i, j, tam, lsup, qh, qm, auxCont: inteiro
    aux, caract: caractere
    mh, mm: real
    existe: logico

Inicio
    lsup <- 30
    qh <- 0
    qm <- 0
    mh <- 0
    mm <- 0
    existe <- falso

    para i de 1 ate lsup faca
        escreval("FUNCIONÁRIO", i)
        escreva("Insira o nome: ")
        leia(funcionario[i].nome)
        aux <- ""
        tam <- compr(funcionario[i].nome)
        
        para j de 1 ate tam faca
            caract <- copia(funcionario[i].nome; j; 1)
            se (caract <> " ") entao
                aux <- aux + caract
            fimse
        fimpara
        
        enquanto (aux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(funcionario[i].nome)
            aux <- ""
            tam <- compr(funcionario[i].nome)
            
            para j de 1 ate tam faca
                caract <- copia(funcionario[i].nome; j; 1)
                se (caract <> " ") entao
                    aux <- aux + caract
                fimse
            fimpara
        fimenquanto
        
        escreva("Insira o sexo (F - Feminino; M - Masculino): ")
        leia(funcionario[i].sexo)
        funcionario[i].sexo <- maiusc(funcionario[i].sexo)
        
        enquanto ((funcionario[i].sexo <> "F") e (funcionario[i].sexo <> "M")) faca
            escreva("Insira 'F' ou 'M': ")
            leia(funcionario[i].sexo)
            funcionario[i].sexo <- maiusc(funcionario[i].sexo)
        fimenquanto
        
        escreva("Insira a idade: ")
        leia(funcionario[i].idade)
        
        enquanto (funcionario[i].idade <= 0) faca
            escreva("Insira uma idade maior que 0: ")
            leia(funcionario[i].idade)
        fimenquanto
        
        escreva("Insira o salário: ")
        leia(funcionario[i].salario)
        
        enquanto (funcionario[i].salario <= 0) faca
            escreva("Insira um salário maior que 0: ")
            leia(funcionario[i].salario)
        fimenquanto
        
        se (funcionario[i].sexo = "F") entao
            funcionario[i].sexo <- "Feminino"
            qm <- qm + 1
            mm <- mm + funcionario[i].salario
        senao
            funcionario[i].sexo <- "Masculino"
            qh <- qh + 1
            mh <- mh + funcionario[i].salario
        fimse
        
        escreval
    fimpara
    
    se (qm > 0) entao
        auxCont <- 0
        mm <- mm/qm
        para i de 1 ate lsup faca
            se (funcionario[i].sexo = "Feminino") entao
                auxCont <- auxCont + 1
                escreval("DADOS DA ", auxCont,"ª FUNCIONÁRIA:")
                escreval
                escreval("Nome: ", funcionario[i].nome,".")
                escreval("Idade:", funcionario[i].idade," anos.")
                escreval("Salário: R$", funcionario[i].salario:6:2,".")
                escreval
                se (funcionario[i].idade > 30) entao
                    existe <- verdadeiro
                fimse
            fimse
        fimpara
    senao
        escreval("Não foram inseridas funcionárias no sistema.")
        escreval
    fimse
    
    se (qh > 0) entao
        auxCont <- 0
        mh <- mh/qh
        para i de 1 ate lsup faca
            se (funcionario[i].sexo = "Masculino") entao
                auxCont <- auxCont + 1
                escreval("DADOS DO ", auxCont,"º FUNCIONÁRIO:")
                escreval
                escreval("Nome: ", funcionario[i].nome,".")
                escreval("Idade:", funcionario[i].idade," anos.")
                escreval("Salário: R$", funcionario[i].salario:6:2,".")
                escreval
            fimse
        fimpara
    senao
        escreval("Não foram inseridos funcionários no sistema.")
        escreval
    fimse
    
    escreval("Média salarial masculina: R$", mh:6:2,".")
    escreval("Média salarial feminina: R$", mm:6:2,".")
    escreval
    
    se (mh > mm) entao
        escreval("A maior média salarial é a dos homens.")
    senao
        se (mh = mm) entao
            escreval("As médias salariais são iguais.")
        senao
            escreval("A maior média salarial é a das mulheres.")
        fimse
    fimse
    
    escreval
    
    se (existe = verdadeiro) entao
        escreval("Reajustes nos salários das funcionárias maiores que 30 anos:")
        escreval
        para i de 1 ate lsup faca
            se ((funcionario[i].sexo = "Feminino") e (funcionario[i].idade > 30)) entao
                escreval("Nome: ", funcionario[i].nome,".")
                escreval("Idade:", funcionario[i].idade," anos.")
                escreval("Salário antigo: R$", funcionario[i].salario:6:2,".")
                funcionario[i].salario <- funcionario[i].salario * (120/100)
                escreval("Salário pós reajuste: R$", funcionario[i].salario:6:2,".")
                escreval
            fimse
        fimpara
    senao
        escreval("Não existem funcionárias maiores que 30 anos. Portanto, não haverá reajuste.")
    fimse
    
Fimalgoritmo
