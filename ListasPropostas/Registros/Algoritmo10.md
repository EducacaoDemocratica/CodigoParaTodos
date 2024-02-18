# Exercício 10

[**Ver Análise**](Analise10.md)

```markdown
Algoritmo "Q10 - Registros"

Tipo TAeroporto = registro
  codigo: inteiro
  nome: caractere
  voosEntrada: inteiro
  voosSaida: inteiro
FimRegistro

Tipo TVoo = registro
  aEntrada: inteiro
  aSaida: inteiro
FimRegistro

Var
  aeroportos: vetor [1..5] de TAeroporto
  voos: vetor [1..10] de TVoo
  nomes: vetor [1..5] de caractere
  i, j, lsupAeroportos, lsupVoos, tam, aux, qEntrada, qSaida: inteiro
  paux, caract, entrada, saida: caractere

Inicio
  lsupAeroportos <- 3
  lsupVoos <- 5
  qEntrada <- 0
  qSaida <- 0

  para i de 1 ate lsupAeroportos faca
    aeroportos[i].codigo <- -1
  fimenquanto

  para i de 1 ate lsupAeroportos faca
    escreva("Insira o código do", i,"º aeroporto: ")
    leia(aeroportos[i].codigo)

    enquanto ((aeroportos[i].codigo < 0) ou (aeroportos[i].codigo > (lsupAeroportos - 1))) faca
      escreva("Insira um valor entre 0 e", (lsupAeroportos - 1),": ")
      leia(aeroportos[i].codigo)
    fimenquanto

    j <- 1

    enquanto (j < lsupAeroportos) faca
      se (j <> i) entao
        enquanto (aeroportos[i].codigo = aeroportos[j].codigo) faca
          escreva("Esse código já está cadastrado: ")
          leia (aeroportos[i].codigo)

          enquanto ((aeroportos[i].codigo < 0) ou (aeroportos[i].codigo > (lsupAeroportos - 1))) faca
            escreva("Insira um valor entre 0 e", (lsupAeroportos - 1),": ")
            leia(aeroportos[i].codigo)
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto
  fimenquanto

  escreva("Insira o nome da cidade do", i,"º aeroporto: ")
  leia(aeroportos[i].nome)
  paux <- ""
  tam <- compr(aeroportos[i].nome)

  para j de 1 ate tam faca
    caract <- copia(aeroportos[i].nome; j; 1)
    se (caract <> " ") entao
      paux <- paux + caract
  fimpara

  enquanto (paux = "") faca
    escreva("Não preencha com espaços vazios: ")
    leia(aeroportos[i].nome)
    paux <- ""
    tam <- compr(aeroportos[i].nome)

    para j de 1 ate tam faca
      caract <- copia(aeroportos[i].nome; j; 1)
      se (caract <> " ") entao
        paux <- paux + caract
    fimpara
  fimenquanto

  nomes[i] <- maiusc(paux)
  j <- 1

  enquanto (j < lsupAeroportos) faca
    se (j <> i) entao
      enquanto (nomes[i] = nomes[j]) faca
        escreva("Esse nome já está cadastrado: ")
        leia (aeroportos[i].nome)
        paux <- ""
        tam <- compr(aeroportos[i].nome)

        para j de 1 ate tam faca
          caract <- copia(aeroportos[i].nome; j; 1)
          se (caract <> " ") entao
            paux <- paux + caract
        fimpara

        enquanto (paux = "") faca
          escreva("Não preencha com espaços vazios: ")
          leia(aeroportos[i].nome)
          paux <- ""
          tam <- compr(aeroportos[i].nome)

          para j de 1 ate tam faca
            caract <- copia(aeroportos[i].nome; j; 1)
            se (caract <> " ") entao
              paux <- paux + caract
          fimpara
        fimenquanto
      fimenquanto
    fimse

    j <- j + 1
  fimenquanto

  j <- 1
  escreva("Insira a quantidade de voos que chegam: ")
  leia(aeroportos[i].voosEntrada)

  enquanto (aeroportos[i].voosEntrada <= 0) faca
    escreva("Insira um valor maior que 0: ")
    leia(aeroportos[i].voosEntrada)
  fimenquanto

  qEntrada <- qEntrada + aeroportos[i].voosEntrada
  escreva("Insira a quantidade de voos que saem: ")
  leia(aeroportos[i].voosSaida)

  enquanto (aeroportos[i].voosSaida <= 0) faca
    escreva("Insira um valor maior que 0: ")
    leia(aeroportos[i].voosSaida)
  fimenquanto

  qSaida <- qSaida + aeroportos[i].voosSaida
  escreval
fimenquanto

i <- 0
enquanto ((i < lsupVoos) e (qEntrada > 0) e (qSaida > 0)) faca
  aux <- 0

  se ((qEntrada = 1) e (qSaida = 1)) entao
    para j de 1 ate lsupAeroportos faca
      se ((aeroportos[j].voosEntrada = 1) e (aeroportos[j].voosSaida = 1)) entao
        aux <- j
      fimse
    fimenquanto
  fimse

  se (aux <> 0) entao
    qEntrada <- 0
  senao
    i <- i + 1
    escreval("VOO", i)
    escreva("Insira o código do aeroporto de entrada: ")
    leia(voos[i].aEntrada)

    enquanto ((voos[i].aEntrada < 0) ou (voos[i].aEntrada > (lsupAeroportos - 1))) faca
      escreva("Insira um valor entre 0 e", (lsupAeroportos - 1),": ")
      leia(voos[i].aEntrada)
    fimenquanto

    para j de 1 ate lsupAeroportos faca
      se (voos[i].aEntrada = aeroportos[j].codigo) entao
        aux <- j
      fimse
    fimenquanto

    enquanto (aeroportos[aux].voosEntrada = 0) faca
      escreva("Esse aeroporto não possui voos de embarque. Insira outro: ")
      leia(voos[i].aEntrada)

      enquanto ((voos[i].aEntrada < 0) ou (voos[i].aEntrada > (lsupAeroportos - 1))) faca
        escreva("Insira um valor entre 0 e", (lsupAeroportos - 1),": ")
        leia(voos[i].aEntrada)
      fimenquanto

      para j de 1 ate lsupAeroportos faca
        se (voos[i].aEntrada = aeroportos[j].codigo) entao
          aux <- j
        fimse
      fimenquanto
    fimenquanto

    aeroportos[aux].voosEntrada <- aeroportos[aux].voosEntrada - 1
    qEntrada <- qEntrada - 1

    escreva("Insira o código do aeroporto de saída: ")
    leia(voos[i].aSaida)

    enquanto ((voos[i].aSaida < 0) ou (voos[i].aSaida > (lsupAeroportos - 1)) ou (voos[i].aSaida = voos[i].aEntrada)) faca
      se (voos[i].aSaida = voos[i].aEntrada) entao
        escreva("O aeroporto de entrada e de saída devem ser diferentes: ")
      senao
        escreva("Insira um valor entre 0 e", (lsupAeroportos - 1),": ")
      fimse

      leia(voos[i].aSaida)
    fimenquanto

    para j de 1 ate lsupAeroportos faca
      se (voos[i].aSaida = aeroportos[j].codigo) entao
        aux <- j
      fimse
    fimenquanto

    enquanto (aeroportos[aux].voosSaida = 0) faca
      escreva("Esse aeroporto não possui voos de desembarque. Insira outro: ")
      leia(voos[i].aSaida)

      enquanto ((voos[i].aSaida < 0) ou (voos[i].aSaida > (lsupAeroportos - 1)) ou (voos[i].aSaida = voos[i].aEntrada)) faca
        se (voos[i].aSaida = voos[i].aEntrada) entao
          escreva("O aeroporto de entrada e de saída devem ser diferentes: ")
        senao
          escreva("Insira um valor entre 0 e", (lsupAeroportos - 1),": ")
        fimse

        leia(voos[i].aSaida)
      fimenquanto

      para j de 1 ate lsupAeroportos faca
        se (voos[i].aSaida = aeroportos[j].codigo) entao
          aux <- j
        fimse
      fimenquanto
    fimenquanto

    aeroportos[aux].voosSaida <- aeroportos[aux].voosSaida - 1
    qSaida <- qSaida - 1
  fimse

  escreval
fimenquanto

lsupVoos <- i

se ((qEntrada = 0) ou (qSaida = 0)) entao
  escreval("Não é possível realizar mais voos porque não existem")
  escreval("vagas de embarque ou desembarque entre os aeroportos.")
fimse

escreval

para i de 1 ate lsupAeroportos faca
  escreval("AEROPORTO", i)
  escreval("Código: ", aeroportos[i].codigo,".")
  escreval("Nome: ", aeroportos[i].nome,".")
  escreval("Voos de entrada:", aeroportos[i].voosEntrada,".")
  escreval("Voos de saída:", aeroportos[i].voosSaida,".")
  escreval
fimenquanto

para i de 1 ate lsupVoos faca
  para j de 1 ate lsupAeroportos faca
    se (voos[i].aEntrada = aeroportos[j].codigo) entao
      entrada <- aeroportos[j].nome
    fimse

    se (voos[i].aSaida = aeroportos[j].codigo) entao
      saida <- aeroportos[j].nome
    fimse
  fimenquanto

  escreval("VOO", i)
  escreval("Entrada: ", entrada,". (CÓD", voos[i].aEntrada,").")
  escreval("Saída: ", saida,". (CÓD", voos[i].aSaida,").")
  escreval
fimenquanto

Fimalgoritmo
