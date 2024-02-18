# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
fimRegistro

Var
    aluno: TAluno
    i, tam, ano: inteiro
    aux, caract: caractere

Inicio
    escreva("Insira o nome do aluno: ")
    leia(aluno.nome)
    aux <- ""
    tam <- compr(aluno.nome)
    
    para i de 1 ate tam faca
        caract <- copia(aluno.nome; i; 1)
        se (caract <> " ") entao
            aux <- aux + caract
        fimse
    fimpara
    
    enquanto (aux = "") faca
        escreva("Não preencha com espaços vazios: ")
        leia(aluno.nome)
        aux <- ""
        tam <- compr(aluno.nome)
        
        para i de 1 ate tam faca
            caract <- copia(aluno.nome; i; 1)
            se (caract <> " ") entao
                aux <- aux + caract
            fimse
        fimpara
    fimenquanto
    
    escreva("Insira a idade do aluno: ")
    leia(aluno.idade)
    
    enquanto (aluno.idade <= 0) faca
        escreva("Insira uma idade maior que 0: ")
        leia(aluno.idade)
    fimenquanto
    
    escreva("Insira o ano atual: ")
    leia(ano)
    
    enquanto ((ano <= 0) ou (ano <= aluno.idade)) faca
        se (ano <= 0) entao
            escreva("Insira um ano maior que 0: ")
        senao
            escreva("O ano deve ser maior que a idade do aluno: ")
        fimse
        leia(ano)
    fimenquanto
    
    escreval
    escreval("DADOS DO ALUNO")
    escreval
    escreval("Nome: ", aluno.nome)
    escreval("Ano de nascimento:", ano - aluno.idade)
Fimalgoritmo
