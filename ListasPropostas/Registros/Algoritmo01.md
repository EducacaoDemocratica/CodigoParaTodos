# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - Registros"

Tipo TAluno = registro
  nome: caractere
  matematica: real
  portugues: real
  fisica: real
  quimica: real
  situacao: caractere
FimRegistro

Var
  aluno: vetor [1..35] de TAluno
  auxAluno: TAluno
  port, mat, fis, qui: vetor [1..35, 1..4] de real
  i, j, tam, lsup, lsupn, apv: inteiro
  aux, caract: caractere
  apvport, apvmat, apvfis, apvqui, rpvport, rpvmat, rpvfis, rpvqui: logico

Inicio
  lsup <- 35
  lsupn <- 4
  apvport <- falso
  apvmat <- falso
  apvfis <- falso
  apvqui <- falso
  rpvport <- falso
  rpvmat <- falso
  rpvfis <- falso
  rpvqui <- falso

  para i de 1 ate lsup faca
    apv <- 0
    escreval("ALUNO", i)
    escreva("Insira o nome: ")
    leia(aluno[i].nome)

    aux <- ""
    tam <- compr(aluno[i].nome)

    para j de 1 ate tam faca
      caract <- copia(aluno[i].nome, j, 1)
      se (caract <> " ") entao
        aux <- aux + caract
      fimse
    fimpara

    enquanto (aux = "") faca
      escreva("Não preencha com espaços vazios: ")
      leia(aluno[i].nome)
      aux <- ""
      tam <- compr(aluno[i].nome)

      para j de 1 ate tam faca
        caract <- copia(aluno[i].nome, j, 1)
        se (caract <> " ") entao
          aux <- aux + caract
        fimse
      fimpara
    fimenquanto

    escreval
    escreval("MATEMÁTICA")

    para j de 1 ate lsupn faca
      escreva("Insira a nota do", j, "º bimestre: ")
      leia(mat[i, j])

      enquanto ((mat[i, j] < 0) ou (mat[i, j] > 25)) faca
        se (mat[i, j] < 0) entao
          escreva("Insira um valor a partir de 0: ")
        senao
          escreva("A nota deve estar entre 0 e 25: ")
        fimse
        leia(mat[i, j])
      fimenquanto

      aluno[i].matematica <- aluno[i].matematica + mat[i, j]
    fimpara

    se (aluno[i].matematica >= 60) entao
      apv <- apv + 1
      apvmat <- verdadeiro
    senao
      se (aluno[i].matematica < 40) entao
        rpvmat <- verdadeiro
      fimse
    fimse

    escreval
    escreval("PORTUGUÊS")

    para j de 1 ate lsupn faca
      escreva("Insira a nota do", j, "º bimestre: ")
      leia(port[i, j])

      enquanto ((port[i, j] < 0) ou (port[i, j] > 25)) faca
        se (port[i, j] < 0) entao
          escreva("Insira um valor a partir de 0: ")
        senao
          escreva("A nota deve estar entre 0 e 25: ")
        fimse
        leia(port[i, j])
      fimenquanto

      aluno[i].portugues <- aluno[i].portugues + port[i, j]
    fimpara

    se (aluno[i].portugues >= 60) entao
      apv <- apv + 1
      apvport <- verdadeiro
    senao
      se (aluno[i].portugues < 40) entao
        rpvport <- verdadeiro
      fimse
    fimse

    escreval
    escreval("FÍSICA")

    para j de 1 ate lsupn faca
      escreva("Insira a nota do", j, "º bimestre: ")
      leia(fis[i, j])

      enquanto ((fis[i, j] < 0) ou (fis[i, j] > 25)) faca
        se (fis[i, j] < 0) entao
          escreva("Insira um valor a partir de 0: ")
        senao
          escreva("A nota deve estar entre 0 e 25: ")
        fimse
        leia(fis[i, j])
      fimenquanto

      aluno[i].fisica <- aluno[i].fisica + fis[i, j]
    fimpara

    se (aluno[i].fisica >= 60) entao
      apv <- apv + 1
      apvfis <- verdadeiro
    senao
      se (aluno[i].fisica < 40) entao
        rpvfis <- verdadeiro
      fimse
    fimse

    escreval
    escreval("QUÍMICA")

    para j de 1 ate lsupn faca
      escreva("Insira a nota do", j, "º bimestre: ")
      leia(qui[i, j])

      enquanto ((qui[i, j] < 0) ou (qui[i, j] > 25)) faca
        se (qui[i, j] < 0) entao
          escreva("Insira um valor a partir de 0: ")
        senao
          escreva("A nota deve estar entre 0 e 25: ")
        fimse
        leia(qui[i, j])
      fimenquanto

      aluno[i].quimica <- aluno[i].quimica + qui[i, j]
    fimpara

    se (aluno[i].quimica >= 60) entao
      apv <- apv + 1
      apvqui <- verdadeiro
    senao
      se (aluno[i].quimica < 40) entao
        rpvqui <- verdadeiro
      fimse
    fimse

    se (apv = 0) entao
      aluno[i].situacao <- "REPROVADO"
    senao
      se (apv = 4) entao
        aluno[i].situacao <- "APROVADO"
      senao
        aluno[i].situacao <- "EM RECUPERAÇÃO"
      fimse
    fimse

    escreval
  fimpara

  para j de (lsup - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (maiusc(aluno[i].nome) > maiusc(aluno[i + 1].nome)) entao
        auxAluno <- aluno[i]
        aluno[i] <- aluno[i + 1]
        aluno[i + 1] <- auxAluno
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    escreval("DADOS DO", i, "º ALUNO")
    escreval
    escreval("Nome: ", aluno[i].nome)
    escreval("Matemática:", aluno[i].matematica)
    escreval("Português:", aluno[i].portugues)
    escreval("Física:", aluno[i].fisica)
    escreval("Química:", aluno[i].quimica)
    escreval("Situação: ", aluno[i].situacao)
    escreval
  fimpara

  se (apvmat = verdadeiro) entao
    escreval("APROVADOS EM MATEMÁTICA: ")
    escreval
    para i de 1 ate lsup faca
      se (aluno[i].matematica >= 60) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS APROVADOS EM MATEMÁTICA!")
  fimse

  escreval

  se (apvport = verdadeiro) entao
    escreval("APROVADOS EM PORTUGUÊS: ")
    escreval
    para i de 1 ate lsup faca
      se (aluno[i].portugues >= 60) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS APROVADOS EM PORTUGUÊS!")
  fimse

  escreval

  se (apvfis = verdadeiro) entao
    escreval("APROVADOS EM FÍSICA: ")
    escreval
    para i de 1 ate lsup faca
      se (aluno[i].fisica >= 60) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS APROVADOS EM FÍSICA!")
  fimse

  escreval

  se (apvqui = verdadeiro) entao
    escreval("APROVADOS EM QUÍMICA: ")
    escreval
    para i de 1 ate lsup faca
      se (aluno[i].portugues >= 60) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS APROVADOS EM QUÍMICA!")
  fimse

  escreval

  se (rpvmat = verdadeiro) entao
    escreval("RECUPERAÇÃO EM MATEMÁTICA: ")
    escreval
    para i de 1 ate lsup faca
      se ((aluno[i].matematica >= 40) e (aluno[i].matematica < 60)) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS EM RECUPERAÇÃO EM MATEMÁTICA!")
  fimse

  escreval

  se (rpvport = verdadeiro) entao
    escreval("RECUPERAÇÃO EM PORTUGUÊS: ")
    escreval
    para i de 1 ate lsup faca
      se ((aluno[i].portugues >= 40) e (aluno[i].portugues < 60)) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS EM RECUPERAÇÃO EM PORTUGUÊS!")
  fimse

  escreval

  se (rpvfis = verdadeiro) entao
    escreval("RECUPERAÇÃO EM FÍSICA: ")
    escreval
    para i de 1 ate lsup faca
      se ((aluno[i].fisica >= 40) e (aluno[i].fisica < 60)) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS EM RECUPERAÇÃO EM FÍSICA!")
  fimse

  escreval

  se (rpvqui = verdadeiro) entao
    escreval("RECUPERAÇÃO EM QUÍMICA: ")
    escreval
    para i de 1 ate lsup faca
      se ((aluno[i].quimica >= 40) e (aluno[i].quimica < 60)) entao
        escreval(aluno[i].nome)
      fimse
    fimpara
  senao
    escreval("NÃO HOUVERAM ALUNOS EM RECUPERAÇÃO EM QUÍMICA!")
  fimse

Fimalgoritmo
