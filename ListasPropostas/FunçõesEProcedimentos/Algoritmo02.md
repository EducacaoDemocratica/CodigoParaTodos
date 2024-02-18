# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - FuncaoProcedimento"

Tipo TFuncionario = registro
  nome: caractere
  anos: inteiro
  filhos: inteiro
  salarioAtual: real
  salarioNovo: real
fimRegistro

funcao calculaSalario(salarioAtual: real; anos, filhos: inteiro): real
Var
  salarioNovo: real
Inicio
  se (salarioAtual <= 1200) entao
    salarioNovo <- salarioAtual * (130/100)
  senao
    se (salarioAtual <= 2500) entao
      salarioNovo <- salarioAtual * (120/100)
    senao
      salarioNovo <- salarioAtual * (110/100)
    fimse
  fimse

  salarioNovo <- salarioNovo + (salarioAtual * (25/10000) * anos) + (salarioAtual * (1/100) * filhos)
  retorne salarioNovo
fimFuncao

funcao verificaPalavra(nome: caractere): caractere
Var
  palavra, caract: caractere
  i: inteiro
Inicio
  palavra <- ""
  para i de 1 ate compr(nome) faca
    caract <- copia(nome; i; 1)
    se (caract <> " ") entao
      palavra <- palavra + caract
    fimse
  fimpara
  retorne palavra
fimFuncao

funcao leNumero(): inteiro
Var
  n: inteiro
Inicio
  leia(n)
  enquanto (n < 0) faca
    escreva("Insira um valor maior/igual a 0: ")
    leia(n)
  fimenquanto
  retorne n
fimFuncao

procedimento leiaFuncionarios()
Var
  i, filhos, anos: inteiro
Inicio
  lsup <- 5
  para i de 1 ate lsup faca
    escreval("FUNCIONÁRIO ", i)
    escreva("Insira o nome: ")
    leia(funcionario[i].nome)
    enquanto (verificaPalavra(funcionario[i].nome) = "") faca
      escreva("Não preencha com espaços vazios: ")
      leia(funcionario[i].nome)
    fimenquanto

    escreva("Insira a quantidade de anos trabalhados: ")
    funcionario[i].anos <- leNumero()
    escreva("Insira a quantidade de filhos em idade escolar: ")
    funcionario[i].filhos <- leNumero()
    escreva("Insira o salário atual: ")
    leia(funcionario[i].salarioAtual)
    enquanto (funcionario[i].salarioAtual <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(funcionario[i].salarioAtual)
    fimenquanto

    funcionario[i].salarioNovo <- calculaSalario(funcionario[i].salarioAtual, funcionario[i].anos, funcionario[i].filhos)
    escreval
  fimpara
fimProcedimento

procedimento ordenaFuncionarios()
Var
  i, j: inteiro
  auxFuncionario: TFuncionario
Inicio
  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (maiusc(funcionario[i].nome) > maiusc(funcionario[i + 1].nome)) entao
        auxFuncionario <- funcionario[i]
        funcionario[i] <- funcionario[i + 1]
        funcionario[i + 1] <- auxFuncionario
      fimse
    fimpara
  fimpara
fimProcedimento

procedimento imprimeFuncionarios()
Var
  i: inteiro
Inicio
  para i de 1 ate lsup faca
    escreval("DADOS DO ", i, "º FUNCIONÁRIO")
    escreval("Nome: ", funcionario[i].nome, ".")
    escreval("Anos empregado: ", funcionario[i].anos, ".")
    escreval("Filhos em idade escolar: ", funcionario[i].filhos, ".")
    escreval("Salário atual: R$ ", funcionario[i].salarioAtual:6:2, ".")
    escreval("Salário novo: R$ ", funcionario[i].salarioNovo:6:2, ".")
    escreval
  fimpara
Fimalgoritmo
