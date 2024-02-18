# Exercício 57

[**Ver Análise**](Analise57.md)

```markdown
Algoritmo "Q57 - Vetor"
arquivo "palavras.txt"

Var
  p: vetor [1..100] de caractere
  ps: caractere
  i, j, k, lsup, tam, vAsc, achou: inteiro
  t: vetor [1..6] de caractere
  tCarac, psCarac: vetor [1..5] de caractere
  acertou: logico

Inicio
  lsup <- 6
  acertou <- falso

  para i de 1 ate 100 faca
    leia(p[i])
  fimpara

  limpatela
  i <- randi(99) + 1
  ps <- p[i]

  para j de 1 ate 5 faca
    psCarac[j] <- copia(ps; j; 1)
  fimpara

  i <- 1
  escreval("NÃO UTILIZE CARACTERES ESPECIAIS")
  escreval

  enquanto ((i <= lsup) e (acertou = falso)) faca
    escreva("Faça a sua", i,"ª tentativa: ")
    leia(t[i])
    tam <- compr(t[i])

    enquanto (tam <> 5) faca
      escreva("Insira uma palavra de 5 caracteres: ")
      leia(t[i])
      tam <- compr(t[i])
    fimenquanto

    t[i] <- maiusc(t[i])

    se (t[i] = ps) entao
      acertou <- verdadeiro
      escreval
    senao
      j <- 1
      enquanto (j <= tam) faca
        tCarac[j] <- copia(t[i]; j; 1)
        vAsc <- asc(tCarac[j])

        se ((vAsc < 65) ou (vAsc > 90)) entao
          escreva("Insira somente letras: ")
          leia(t[i])
          tam <- compr(t[i])

          enquanto (tam <> 5) faca
            escreva("Insira uma palavra de 5 caracteres: ")
            leia(t[i])
            tam <- compr(t[i])
          fimenquanto

          t[i] <- maiusc(t[i])
          j <- 0
        fimse

        j <- j + 1
      fimenquanto

      para j de 1 ate tam faca
        achou <- 0
        para k de 1 ate tam faca
          se (tCarac[j] = psCarac[k]) entao
            achou <- 1
            se (j = k) entao
              achou <- 2
            fimse
          fimse
        fimpara

        se (achou = 0) entao
          tCarac[j] <- "*"
        senao
          se (achou = 1) entao
            tCarac[j] <- minusc(tCarac[j])
          fimse
        fimse
      fimpara

      se (i <> lsup) entao
        escreva(t[i]," -> ")
        para j de 1 ate tam faca
          escreva(tCarac[j])
        fimpara
      fimse

      escreval
    fimse

    i <- i + 1
  fimse

  se (acertou = verdadeiro) entao
    escreval("Parabéns!!! Você acertou.")
  senao
    escreval("Não foi dessa vez...")
  fimse

  escreval("Palavra sorteada: ", ps,".")
Fimalgoritmo
w

//palavras.txt
SAGAZ
AMAGO
NEGRO
EXITO
MEXER
TERMO
NOBRE
SENSO
ALGOZ
AFETO
ETICA
PLENA
MUTUA
TENUE
SUTIL
VIGOR
FAZER
AQUEM
ASSIM
POREM
SECAO
AUDAZ
SANAR
FOSSE
CERNE
INATO
IDEIA
PODER
MORAL
DESDE
MUITO
JUSTO
TORPE
HONRA
SOBRE
QUICA
FUTIL
RAZAO
ANEXO
ETNIA
ICONE
SONHO
EGIDE
TANGE
AMIGO
LAPSO
MUTUO
EXPOR
HAVER
CASAL
HABIL
DENGO
TEMPO
SEARA
ENTAO
PESAR
AVIDO
ARDIL
BOCAL
GENRO
POSSE
CAUSA
COSER
PRAIA
DIZER
CORJA
PROLE
BRADO
DEVER
FOICE
SABER
GRACA
TENAZ
DETEM
CRIVO
APICE
ANIMO
DIGNO
COMUM
ANSIA
TEMOR
CEDER
SENDO
CULTO
ASSAZ
ATROZ
GLEBA
PAUTA
AINDA
MUNDO
CENSO
FUGAZ
ESTAR
VALHA
VICIO
COZER
FORTE
VULGO
DENSO
NENEM