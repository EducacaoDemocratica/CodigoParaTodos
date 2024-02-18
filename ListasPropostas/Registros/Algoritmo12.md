# Exercício 12

[**Ver Análise**](Analise12.md)

```markdown
Algoritmo "Q12 - exRegistros"

Tipo TCliente = Registro
  nome: caractere
  fornecimento: caractere
  vFornecimento: real
  natureza: caractere
  kWhCliente: real
  kWhconsumidos: real
  vTaxa: real
  vConsumo: real
  imposto: real
  total: real
FimRegistro

Var
  clientes: vetor [1..300] de TCliente
  paux, caract: caractere
  nMaior, nRural, nIsento: vetor [1..300] de caractere
  lsup, i, j, tam, aux, qMaior, qRural, qIsento, qBifasica: inteiro
  kWh, iluminacao, bandeira, total, totalIluminacao, maior: real

Inicio
  lsup <- 5
  total <- 0
  totalIluminacao <- 0
  qMaior <- 0
  qRural <- 0
  qIsento <- 0
  qBifasica <- 0

  escreva("Insira o valor do kWh: R$")
  leia(kWh)

  enquanto (kWh <= 0) faca
    escreva("Insira um valor maior que 0: R$")
    leia(kWh)
  fimenquanto

  escreva("Insira o valor da taxa de iluminação pública (%): ")
  leia(iluminacao)

  enquanto (iluminacao <= 0) faca
    escreva("Insira um valor maior que 0: ")
    leia(iluminacao)
  fimenquanto

  iluminacao <- iluminacao / 100

  escreva("Insira o valor da bandeira vigente: R$")
  leia(bandeira)

  enquanto (bandeira <= 0) faca
    escreva("Insira um valor maior que 0: R$")
    leia(bandeira)
  fimenquanto

  escreval

  para i de 1 ate lsup faca
    escreval("DADOS DO", i, "º CLIENTE")
    escreval
    escreva("Insira o nome: ")
    leia(clientes[i].nome)
    paux <- ""
    tam <- compr(clientes[i].nome)

    para j de 1 ate tam faca
      caract <- copia(clientes[i].nome, j, 1)
      se (caract <> " ") entao
        paux <- paux + caract
    fimpara

    enquanto (paux = "") faca
      escreva("Não preencha com espaços vazios: ")
      leia(clientes[i].nome)
      paux <- ""
      tam <- compr(clientes[i].nome)

      para j de 1 ate tam faca
        caract <- copia(clientes[i].nome, j, 1)
        se (caract <> " ") entao
          paux <- paux + caract
      fimpara
    fimenquanto

    clientes[i].nome <- maiusc(paux)
    j <- 1

    enquanto (j < lsup) faca
      se (j <> i) entao
        enquanto (clientes[i].nome = clientes[j].nome) faca
          escreva("Esse nome já está cadastrado: ")
          leia(clientes[i].nome)
          paux <- ""
          tam <- compr(clientes[i].nome)

          para j de 1 ate tam faca
            caract <- copia(clientes[i].nome, j, 1)
            se (caract <> " ") entao
              paux <- paux + caract
          fimpara

          enquanto (paux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(clientes[i].nome)
            paux <- ""
            tam <- compr(clientes[i].nome)

            para j de 1 ate tam faca
              caract <- copia(clientes[i].nome, j, 1)
              se (caract <> " ") entao
                paux <- paux + caract
              fimse
            fimenquanto
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto
  fimenquanto

  escreval

  para i de 1 ate lsup faca
    escreval("--------------------------------------------")
    escreval(i, "º cliente: ", clientes[i].nome, ".")
    escreval(" Classe: ", clientes[i].fornecimento, ".")
    escreval(" Natureza: ", clientes[i].natureza, ".")
    escreval(" kWh consumidos:", clientes[i].kWhconsumidos, ".")
    escreval(" Total: R$", clientes[i].total:6:2, ".")
    escreval
  fimenquanto

  para i de 1 ate lsup faca
    total <- total + clientes[i].total

    se (i = 1) entao
      qMaior <- 1
      maior <- clientes[i].total
      nMaior[qMaior] <- clientes[i].nome
    senao
      se (clientes[i].total > maior) entao
        qMaior <- 1
        maior <- clientes[i].total
        nMaior[qMaior] <- clientes[i].nome
      senao
        se (clientes[i].total = maior) entao
          qMaior <- qMaior + 1
          nMaior[qMaior] <- clientes[i].nome
        fimse
      fimse
    fimse
  fimenquanto

  escreval("--------------------------------------------")
  escreval

  para i de 1 ate lsup faca
    escreval(i, "º cliente: ", clientes[i].nome, ".")
    escreval(" Classe: ", clientes[i].fornecimento, ".")
    escreval(" Natureza: ", clientes[i].natureza, ".")
    escreval(" kWh consumidos:", clientes[i].kWhconsumidos, ".")
    escreval(" Total: R$", clientes[i].total:6:2, ".")
    escreval
  fimenquanto

  escreval("Maior valor final de conta: R$", maior:6:2, ".")
  escreva("Clientes que possuem tal valor: ")

  para i de 1 ate qMaior faca
    se (i = qMaior) entao
      escreval(nMaior[i], ".")
    senao
      escreva(nMaior[i], ", ")
    fimse
  fimenquanto

  escreval
  escreval("Total arrecadado na região: R$", total:6:2, ".")
  escreval

  se (qRural = 0) entao
    escreval("Não houveram clientes que possuem residência rural.")
  senao
    escreva("Clientes que possuem residência rural: ")

    para i de 1 ate qRural faca
      se (i = qRural) entao
        escreval(nRural[i], ".")
      senao
        escreva(nRural[i], ", ")
      fimse
    fimenquanto
  fimse

  escreval

  se (qBifasica = 0) entao
    escreval("Não houveram clientes com classe de fornecimento bifásica.")
  senao
    escreval("Quantidade de clientes que possuem classe bifásica:", qBifasica, ".")
  fimse

  escreval
  escreval("Valor total arrecadado com iluminação pública: R$", totalIluminacao:6:2, ".")

  se (qIsento = 0) entao
    escreval("Não houveram clientes isentos da taxa de iluminação pública.")
  senao
    escreva("Clientes isentos da taxa de iluminação pública: ")

    para i de 1 ate qIsento faca
      se (i = qIsento) entao
        escreval(nIsento[i], ".")
      senao
        escreva(nIsento[i], ", ")
      fimse
    fimenquanto
  fimse

Fimalgoritmo
