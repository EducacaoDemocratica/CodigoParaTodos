# Exercício 03

[**Ver Análise**](Analise03.md)

```markdown
Algoritmo "Q3 - Registros"
Tipo TFuncionario = registro
  nome: caractere
  anos: inteiro
  filhos: inteiro
  salarioatual: real
  salarionovo: real
fimRegistro

Var
  funcionario: vetor [1..35] de TFuncionario
  auxFuncionario: TFuncionario
  i, j, tam, lsup: inteiro
  aux, caract: caractere

Inicio
  lsup <- 5

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

    escreva("Insira a quantidade de anos trabalhados: ")
    leia(funcionario[i].anos)

    enquanto (funcionario[i].anos < 0) faca
      escreva("Insira um valor maior/igual a 0: ")
      leia(funcionario[i].anos)
    fimenquanto

    escreva("Insira a quantidade de filhos em idade escolar: ")
    leia(funcionario[i].filhos)

    enquanto (funcionario[i].filhos < 0) faca
      escreva("Insira um valor maior/igual a 0: ")
      leia(funcionario[i].filhos)
    fimenquanto

    escreva("Insira o salário atual: ")
    leia(funcionario[i].salarioatual)

    enquanto (funcionario[i].salarioatual <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(funcionario[i].salarioatual)
    fimenquanto

    se (funcionario[i].salarioatual <= 1200) entao
      funcionario[i].salarionovo <- funcionario[i].salarioatual * (130/100)
    senao
      se (funcionario[i].salarioatual <= 2500) entao
        funcionario[i].salarionovo <- funcionario[i].salarioatual * (120/100)
      senao
        funcionario[i].salarionovo <- funcionario[i].salarioatual * (110/100)
      fimse
    fimse

    funcionario[i].salarionovo <- funcionario[i].salarionovo +
      (funcionario[i].salarioatual * (25/10000) * funcionario[i].anos) +
      (funcionario[i].salarioatual * (1/100) * funcionario[i].filhos)

    escreval
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (maiusc(funcionario[i].nome) > maiusc(funcionario[i + 1].nome)) entao
        auxFuncionario <- funcionario[i]
        funcionario[i] <- funcionario[i + 1]
        funcionario[i + 1] <- auxFuncionario
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    escreval("DADOS DO", i,"º FUNCIONÁRIO")
    escreval("Nome: ", funcionario[i].nome,".")
    escreval("Anos empregado:", funcionario[i].anos,".")
    escreval("Filhos em idade escolar:", funcionario[i].filhos,".")
    escreval("Salário atual: R$", funcionario[i].salarioatual:6:2,".")
    escreval("Salário novo: R$: ", funcionario[i].salarionovo:6:2,".")
    escreval
  fimpara

Fimalgoritmo
