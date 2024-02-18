# Exercício 08

[**Ver Análise**](Analise08.md)

```markdown
Algoritmo "Q8 - exRegistros"
Tipo TEletrodomestico = registro
  nome: caractere
  potencia: real
  tempoDiario: inteiro
  consumo: real
  consumoRelativo: real
fimRegistro

Var
  eletrodomesticos: vetor [1..5] de TEletrodomestico
  i, j, n, lsup, tam: inteiro
  paux, caract: caractere
  consumoTotal: real

Inicio
  lsup <- 5
  consumoTotal <- 0

  para i de 1 ate lsup faca
    escreva("Insira o nome do", i,"º eletrodoméstico: ")
    leia(eletrodomesticos[i].nome)

    paux <- ""
    tam <- compr(eletrodomesticos[i].nome)

    para j de 1 ate tam faca
      caract <- copia(eletrodomesticos[i].nome; j; 1)
      se (caract <> " ") entao
        paux <- paux + caract
      fimse
    fimpara

    enquanto (paux = "") faca
      escreva("Não preencha com espaços vazios: ")
      leia(eletrodomesticos[i].nome)
      paux <- ""
      tam <- compr(eletrodomesticos[i].nome)

      para j de 1 ate tam faca
        caract <- copia(eletrodomesticos[i].nome; j; 1)
        se (caract <> " ") entao
          paux <- paux + caract
        fimse
      fimpara
    fimenquanto

    eletrodomesticos[i].nome <- maiusc(paux)
    j <- 1

    enquanto (j < lsup) faca
      se (j <> i) entao
        enquanto (eletrodomesticos[i].nome = eletrodomesticos[j].nome) faca
          escreva("Esse nome já está cadastrado: ")
          leia (eletrodomesticos[i].nome)

          paux <- ""
          tam <- compr(eletrodomesticos[i].nome)

          para j de 1 ate tam faca
            caract <- copia(eletrodomesticos[i].nome; j; 1)
            se (caract <> " ") entao
              paux <- paux + caract
            fimse
          fimpara

          enquanto (paux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(eletrodomesticos[i].nome)
            paux <- ""
            tam <- compr(eletrodomesticos[i].nome)

            para j de 1 ate tam faca
              caract <- copia(eletrodomesticos[i].nome; j; 1)
              se (caract <> " ") entao
                paux <- paux + caract
              fimse
            fimpara
          fimenquanto

          eletrodomesticos[i].nome <- maiusc(paux)
        fimenquanto
      fimse
      j <- j + 1
    fimenquanto

    escreva("Insira a potencia do eletrodoméstico: ")
    leia(eletrodomesticos[i].potencia)

    enquanto (eletrodomesticos[i].potencia <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(eletrodomesticos[i].potencia)
    fimenquanto

    escreva("Insira o tempo (horas) ativo por dia: ")
    leia(eletrodomesticos[i].tempoDiario)

    enquanto ((eletrodomesticos[i].tempoDiario <= 0) ou (eletrodomesticos[i].tempoDiario > 24)) faca
      escreva("Insira um valor entre 0 e 24: ")
      leia(eletrodomesticos[i].tempoDiario)
    fimenquanto
  fimenquanto

  escreva("Insira o número de dias: ")
  leia(n)

  enquanto (n <= 0) faca
    escreva("Insira um valor maior que 0: ")
    leia(n)
  fimenquanto

  para i de 1 ate lsup faca
    eletrodomesticos[i].consumo <- eletrodomesticos[i].potencia * eletrodomesticos[i].tempoDiario
    consumoTotal <- consumoTotal + eletrodomesticos[i].consumo
  fimenquanto

  para i de 1 ate lsup faca
    eletrodomesticos[i].consumoRelativo <- eletrodomesticos[i].consumo / consumoTotal * 100
  fimenquanto

  consumoTotal <- consumoTotal * n

  escreval
  escreval("Consumo total da casa:", consumoTotal,"kWh.")
  escreval("Consumo real e relativo de cada eletrodoméstico")
  escreval

  para i de 1 ate lsup faca
    escreval(eletrodomesticos[i].nome,";",
             eletrodomesticos[i].consumo * n,"kWh;",
             eletrodomesticos[i].consumoRelativo:6:2,"%")
  fimenquanto

Fimalgoritmo
