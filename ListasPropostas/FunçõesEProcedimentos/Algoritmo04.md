# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - FuncaoProcedimento"

Tipo TConta = registro
  nome: caractere
  idade: inteiro
  cpf: caractere
  telefone: caractere
  codigo: inteiro
  saldo: real
fimRegistro

funcao menu(): inteiro
Var
  opcao: inteiro
Inicio
  escreval
  escreval("FUNÇÕES DISPONÍVEIS:")
  escreval
  escreval("0 - SAIR")
  escreval("1 - CRIAR CONTA")
  escreval("2 - LISTAR CONTAS")
  escreval("3 - DEPOSITAR")
  escreval("4 - SACAR")
  escreval("5 - GERAR EXTRATO")
  escreval
  escreva("Selecione uma opção: ")
  leia (opcao)
  enquanto ((opcao < 0) ou (opcao > 5)) faca
    escreva("Selecione um número de 0 a 5: ")
    leia (opcao)
  fimenquanto
  retorne opcao
fimFuncao

funcao validaCPF (cpf: caractere): logico
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
      se (r1 < 2) então
        r1 <- 0
      senao
        r1 <- 11 - r1
      fimse
      para i de 1 ate 10 faca
        s2 <- s2 + (ncpf[i] * (12 - i))
      fimpara
      r2 <- s2 mod 11
      se (r2 < 2) então
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

funcao verificaEntradaCPF (cpf: caractere): logico
Var
  j: inteiro
Inicio
  para j de 1 ate i faca
    se ((j <> i) e (contas[j].cpf = cpf)) entao
      retorne falso
    fimse
  fimpara
  retorne verdadeiro
fimFuncao

funcao verificaEntradaTelefone (telefone: caractere): logico
Var
  j: inteiro
Inicio
  para j de 1 ate i faca
    se ((j <> i) e (contas[j].telefone = telefone)) entao
      retorne falso
    fimse
  fimpara
  retorne verdadeiro
fimFuncao

funcao somenteDigitos (telefone: caractere): caractere
Var
  tam, i: inteiro
  p, caract: caractere
Inicio
  p <- ""
  tam <- compr(telefone)
  para i de 1 ate tam faca
    caract <- copia(telefone; i; 1)
    se ((asc(caract) >= 48) e (asc(caract) <= 57)) entao
      p <- p + caract
    fimse
  fimpara
  retorne p
fimFuncao

funcao procurarConta(): inteiro
Var
  cod: inteiro
Inicio
  se (i = 0) entao
    escreval("Não existem contas cadastradas!")
    retorne 0
  senao
    escreva("Insira o código da conta: ")
    leia(cod)
    enquanto ((cod <= 0) ou (cod > i)) faca
      escreva("Código não encontrado: ")
      leia(cod)
    fimenquanto
    retorne cod
  fimse
fimFuncao

funcao lerValor(): real
Var
  valor: real
Inicio
  escreva("Insira o valor da transferência: ")
  leia(valor)
  enquanto (valor <= 0) faca
    escreva("Insira um valor maior que 0: ")
    leia(valor)
  fimenquanto
  retorne valor
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

procedimento lerConta()
Var
  Inicio
    se (i + 1 > 30) entao
      escreval("Não é possivel criar mais contas: ")
    senao
      i <- i + 1
      escreval
      escreva("Insira a idade: ")
      leia(contas[i].idade)
      enquanto (contas[i].idade < 18) faca
        escreva("A idade mínima para abrir uma conta é 18 anos: ")
        leia(contas[i].idade)
      fimenquanto
      escreva("Insira o nome: ")
      leia(contas[i].nome)
      enquanto (verificaPalavra(contas[i].nome) = "") faca
        escreva("Não preecnha com espaços vazios: ")
        leia(contas[i].nome)
      fimenquanto
      escreva("Insira o CPF (somente números): ")
      leia(contas[i].cpf)
      enquanto ((verificaEntradaCPF(contas[i].cpf) = falso) ou
             (validaCPF(contas[i].cpf) = falso)) faca
        se (verificaEntradaCPF(contas[i].cpf) = falso) entao
          escreva("CPF já usado. Insira outro (somente números): ")
        senao
          escreva("CPF inválido. Insira outro (somente números): ")
        fimse
        leia(contas[i].cpf)
      fimenquanto
      escreval("Insira o telefone ")
      escreva("(somente os 2 números do DDD e os 9 restantes): ")
      leia(contas[i].telefone)
      contas[i].telefone <- somenteDigitos(contas[i].telefone)
      enquanto ((verificaEntradaTelefone(contas[i].telefone) = falso)
             ou (compr(contas[i].telefone) <> 11)) faca
        se (verificaEntradaTelefone(contas[i].telefone) = falso) entao
          escreva("Telefone já usado. Insira outro")
        senao
          escreva("Telefone inválido. Insira outro")
        fimse
        leia(contas[i].telefone)
      fimenquanto
      contas[i].codigo <- i
      escreval
      escreval("CONTA CRIADA COM SUCESSO:")
      gerarExtrato(i)
    fimse
fimProcedimento

procedimento listarContas()
Var
  j: inteiro
Inicio
  se (i = 0) entao
    escreval("Não existem contas cadastradas!")
  senao
    para j de 1 ate i faca
      escreval
      escreval("CONTA", i)
      escreval("Código:", contas[j].codigo,".")
      escreval("Cliente: ", contas[j].nome,".")
      escreval("Idade:", contas[j].idade," anos.")
      escreval("CPF: ", contas[j].cpf,".")
      escreval("Telefone: ", contas[j].telefone,".")
      escreval("Saldo: R$", contas[j].saldo:6:2,".")
    fimpara
  fimse
fimProcedimento

procedimento gerarExtrato(cod: inteiro)
Var
  Inicio
    se (cod <> 0) entao
      escreval
      escreval("Código:", contas[cod].codigo,".")
      escreval("Cliente: ", contas[cod].nome," - ", contas[cod].cpf)
      escreval("Saldo: R$", contas[cod].saldo:6:2,".")
    fimse
fimProcedimento

procedimento depositar()
Var
  cod: inteiro
  valor: real
Inicio
  cod <- procurarConta()
  se (cod <> 0) entao
    valor <- lerValor()
    escreval("Antes do depósito: ")
    gerarExtrato(cod)
    contas[cod].saldo <- contas[cod].saldo + valor
    escreval("Após o depósito: ")
    gerarExtrato(cod)
  fimse
fimProcedimento

procedimento sacar()
Var
  cod: inteiro
  valor: real
Inicio
  cod <- procurarConta()
  se (cod <> 0) entao
    valor <- lerValor()
    se (contas[cod].saldo >= valor) entao
      escreval("Antes do saque: ")
      gerarExtrato(cod)
      contas[cod].saldo <- contas[cod].saldo - valor
      escreval("Após o saque: ")
      gerarExtrato(cod)
    senao
      escreval("Não é possível realizar o saque pois o saldo da conta é insuficiente!")
    fimse
  fimse
fimProcedimento

Var
  contas: vetor [1..30] de TConta
  i, f: inteiro
Inicio
  f <- menu()
  enquanto (f <> 0) faca
    se (f = 1) entao
      lerConta()
    senao
      se (f = 2) entao
        listarContas()
      senao
        se (f = 3) entao
          depositar()
        senao
          se (f = 4) entao
            sacar()
          senao
            gerarExtrato(procurarConta())
          fimse
        fimse
      fimse
    fimse
    fimse
    fimse
    f <- menu()
  fimenquanto
Fimalgoritmo
