# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - Registros"
Tipo TData = registro
  dia: inteiro
  mes: inteiro
  ano: inteiro
fimRegistro

Var
  texto, aux, caract: caractere
  horario: THorario
  data: TData
  diavalido, bissexto: logico
  i, tam: inteiro

Inicio
  diavalido <- verdadeiro

  escreval("Insira o horário do compromisso")
  escreval
  escreva("Insira a hora: ")
  leia(horario.hora)

  enquanto ((horario.hora < 0) ou (horario.hora > 23)) faca
    escreva("Insira um valor de 0 a 23: ")
    leia(horario.hora)
  fimenquanto

  escreva("Insira o minuto: ")
  leia(horario.minuto)

  enquanto ((horario.minuto < 0) ou (horario.minuto > 59)) faca
    escreva("Insira um valor de 0 a 59: ")
    leia(horario.minuto)
  fimenquanto

  escreva("Insira o segundo: ")
  leia(horario.segundo)

  enquanto ((horario.segundo < 0) ou (horario.segundo > 59)) faca
    escreva("Insira um valor de 0 a 59: ")
    leia(horario.segundo)
  fimenquanto

  escreval
  escreval("Insira a data do compromisso")
  escreval
  escreva("Insira o ano: ")
  leia(data.ano)

  enquanto (data.ano <= 0) faca
    escreva("Insira um valor maior que 0: ")
    leia(data.ano)
  fimenquanto

  se ((data.ano mod 4 = 0) e (data.ano mod 100 <> 0)) entao
    bissexto <- verdadeiro
  senao
    bissexto <- falso
  fimse

  escreva("Insira o mês: ")
  leia(data.mes)

  enquanto ((data.mes <= 0) ou (data.mes > 12)) faca
    escreva("Insira um valor de 1 a 12: ")
    leia(data.mes)
  fimenquanto

  escreva("Insira o dia: ")
  leia(data.dia)

  se ((data.dia <= 0) ou (data.dia > 31)) entao
    diavalido <- falso
  fimse

  se ((data.dia = 29) e (data.mes = 2) e (bissexto = verdadeiro)) entao
    diavalido <- verdadeiro
  senao
    se ((data.dia = 29) e (data.mes = 2) e (bissexto = falso)) entao
      diavalido <- falso
    senao
      se ((data.dia = 31) e ( ((data.mes <= 7) e (data.mes mod 2 = 0)) ou ((data.mes >= 8) e (data.mes mod 2 = 1)) )) entao
        diavalido <- falso
      fimse
    fimse
  fimse

  enquanto (diavalido = falso) faca
    se ((data.dia <= 0) ou (data.dia > 31)) entao
      escreva("Insira valores de 1 a 31: ")
    fimse

    se ((data.dia = 29) e (data.mes = 2) e (bissexto = falso)) entao
      escreva("O ano", data.ano," não é bissexto: ")
    senao
      se ((data.dia = 31) e ( ((data.mes <= 7) e (data.mes mod 2 = 0)) ou ((data.mes >= 8) e (data.mes mod 2 = 1)) )) entao
        escreva("O mes", data.mes," possui apenas 30 dias: ")
      fimse
    fimse

    leia(data.dia)
    diavalido <- verdadeiro

    se ((data.dia <= 0) ou (data.dia > 31)) entao
      diavalido <- falso
    fimse

    se ((data.dia = 29) e (data.mes = 2) e (bissexto = falso)) entao
      diavalido <- falso
    senao
      se ((data.dia = 31) e ( ((data.mes <= 7) e (data.mes mod 2 = 0)) ou ((data.mes >= 8) e (data.mes mod 2 = 1)) )) entao
        diavalido <- falso
      fimse
    fimse
  fimenquanto

  escreval
  escreva("Insira o texto do compromisso: ")
  leia(texto)
  aux <- ""
  tam <- compr(texto)

  para i de 1 ate tam faca
    caract <- copia(texto; i; 1)
    se (caract <> " ") entao
      aux <- aux + caract
    fimse
  fimpara

  enquanto (aux = "") faca
    escreva("Não preencha com espaços vazios: ")
    leia(texto)
    aux <- ""
    tam <- compr(texto)

    para i de 1 ate tam faca
      caract <- copia(texto; i; 1)
      se (caract <> " ") entao
        aux <- aux + caract
      fimse
    fimpara
  fimenquanto

  escreval
  escreval("Dados do compromisso")
  escreval
  escreval("Data:", data.dia," /", data.mes," /", data.ano,".")
  escreval("Horário:",
           horario.hora,"h",
           horario.minuto,"min",
           horario.segundo,"s.")
  escreval("Descrição: ", texto,"")

Fimalgoritmo
