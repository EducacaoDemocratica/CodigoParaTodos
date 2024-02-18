# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - Registros"
Tipo TData = registro
  dia: inteiro
  mes: inteiro
  ano: inteiro
fimRegistro

Var
  data: vetor [1..2] de TData
  aux: TData
  diavalido, bissexto: logico
  i, tam, maior, menor, q, mes: inteiro
  dias: vetor [1..12] de inteiro

Inicio
  q <- 0

  para i de 1 ate 12 faca
    se (((i<= 7) e (i mod 2 = 0)) ou ((i >= 8) e (i mod 2 = 1)))
    entao
      dias[i] <- 30
    senao
      dias[i] <- 31
    fimse
  fimpara

  para i de 1 ate 2 faca
    diavalido <- verdadeiro

    escreval
    escreval("Dados da",i,"ª data")
    escreval

    escreva("Insira o ano: ")
    leia(data[i].ano)

    enquanto (data[i].ano <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(data[i].ano)
    fimenquanto

    se ((data[i].ano mod 4 = 0) e (data[i].ano mod 100 <> 0))
      bissexto <- verdadeiro
    senao
      bissexto <- falso
    fimse

    escreva("Insira o mês: ")
    leia(data[i].mes)

    enquanto ((data[i].mes <= 0) ou (data[i].mes > 12)) faca
      escreva("Insira um valor de 1 a 12: ")
      leia(data[i].mes)
    fimenquanto

    escreva("Insira o dia: ")
    leia(data[i].dia)

    se ((data[i].dia <= 0) ou (data[i].dia > 31)) entao
      diavalido <- falso
    fimse

    se ((data[i].dia = 29) e (data[i].mes = 2) e (bissexto = verdadeiro)) entao
      diavalido <- verdadeiro
    senao
      se ((data[i].dia = 29) e (data[i].mes = 2) e (bissexto = falso)) entao
        diavalido <- falso
      senao
        se ((data[i].dia = 31) e ( ((data[i].mes <= 7) e (data[i].mes mod 2 = 0)) ou ((data[i].mes >= 8) e (data[i].mes mod 2 = 1)) )) entao
          diavalido <- falso
        fimse
      fimse
    fimse

    enquanto (diavalido = falso) faca
      se ((data[i].dia <= 0) ou (data[i].dia > 31)) entao
        escreva("Insira valores de 1 a 31: ")
      fimse

      se ((data[i].dia = 29) e (data[i].mes = 2) e (bissexto = falso)) entao
        escreva("O ano", data[i].ano," não é bissexto: ")
      senao
        se ((data[i].dia = 31) e ( ((data[i].mes <= 7) e (data[i].mes mod 2 = 0)) ou ((data[i].mes >= 8) e (data[i].mes mod 2 = 1)) )) entao
          escreva("O mes", data[i].mes," possui apenas 30 dias: ")
        fimse
      fimse

      leia(data[i].dia)
      diavalido <- verdadeiro

      se ((data[i].dia <= 0) ou (data[i].dia > 31)) entao
        diavalido <- falso
      fimse

      se ((data[i].dia = 29) e (data[i].mes = 2) e (bissexto = falso)) entao
        diavalido <- falso
      senao
        se ((data[i].dia = 31) e ( ((data[i].mes <= 7) e (data[i].mes mod 2 = 0)) ou ((data[i].mes >= 8) e (data[i].mes mod 2 = 1)) )) entao
          diavalido <- falso
        fimse
      fimse
    fimenquanto

    escreval
  fimpara

  se ((data[1].ano <> data[2].ano) e (data[1].ano > data[2].ano)) entao
    aux <- data[2]
    data[2] <- data[1]
    data[1] <- aux
  senao
    se ((data[1].mes <> data[2].mes) e (data[1].mes < data[2].mes)) entao
      aux <- data[2]
      data[2] <- data[1]
      data[1] <- aux
    senao
      se ((data[1].mes = data[2].mes) e (data[1].dia > data[2].dia)) entao
        aux <- data[2]
        data[2] <- data[1]
        data[1] <- aux
      fimse
    fimse
  fimse

  se ((data[2].ano - data[1].ano) > 1) entao
    se ((data[2].ano - data[1].ano) >= 30) entao
      q <- q + 1
    fimse

    menor <- data[1].ano
    maior <- data[2].ano

    enquanto (menor < (maior - 1)) faca
      menor <- menor + 1

      se ((menor mod 4 = 0) e (menor mod 100 <> 0)) entao
        q <- q + 366
      senao
        q <- q + 365
      fimse
    fimenquanto
  fimse

  mes <- data[1].mes
  q <- q + (dias[mes] - data[1].dia)

  enquanto (mes < 12) faca
    mes <- mes + 1

    se (mes = 2) entao
      se ((data[1].ano mod 4 = 0) e (data[1].ano mod 100 <> 0)) entao
        q <- q + 29
      senao
        q <- q + 28
      fimse
    senao
      q <- q + dias[mes]
    fimse
  fimenquanto

  mes <- data[2].mes
  i <- 0

  enquanto (i < (mes - 1)) faca
    i <- i + 1

    se (i = 2) entao
      se ((data[2].ano mod 4 = 0) e (data[2].ano mod 100 <> 0)) entao
        q <- q + 29
      senao
        q <- q + 28
      fimse
    senao
      q <- q + dias[i]
    fimse
  fimenquanto

  q <- q + data[2].dia

  escreval("Existem", q," dias entre", data[1].dia,"/", data[1].mes,"/", data[1].ano," e", data[2].dia,"/", data[2].mes,"/", data[2].ano,".")

Fimalgoritmo
