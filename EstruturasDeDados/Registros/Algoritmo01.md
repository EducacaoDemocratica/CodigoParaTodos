# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - exRegistros"
Tipo TAluno = registro
    nome: caractere
    idade: inteiro
fimRegistro

Var
    aluno: TAluno
    i, tam: inteiro
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
    
    escreval
    escreval("DADOS DO ALUNO(A)")
    escreval
    escreval("Nome: ", aluno.nome)
    escreval("Idade:", aluno.idade)
Fimalgoritmo
