# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - Registros"
Tipo TAluno = registro
  nome: caractere
  matematica: real
  situacao: caractere
fimRegistro

Var
  aluno: vetor [1..20] de TAluno
  mat: vetor [1..20, 1..4] de real
  qacm: vetor [1..4] de inteiro
  nomes: vetor [1..20] de caractere
  media: vetor [1..20] de real
  maior: real
  i, j, k, tam, lsup, lsupn, qapv, qrpv, qrec: inteiro
  aux, caract: caractere

Inicio
  lsup <- 20
  lsupn <- 4
  qapv <- 0
  qrpv <- 0
  qrec <- 0
  k <- 0

  para i de 1 ate lsup faca
    escreval("ALUNO", i)
    escreva("Insira o nome: ")
    leia(aluno[i].nome)

    aux <- ""
    tam <- compr(aluno[i].nome)

    para j de 1 ate tam faca
      caract <- copia(aluno[i].nome; j; 1)
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
        caract <- copia(aluno[i].nome; j; 1)
        se (caract <> " ") entao
          aux <- aux + caract
        fimse
      fimpara
    fimenquanto

    escreval

    para j de 1 ate lsupn faca
      escreva("Nota de matemática do", j,"º bimestre: ")
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

    se (i = 1) entao
      k <- k + 1
      maior <- aluno[i].matematica
      nomes[k] <- aluno[i].nome
    senao
      se (aluno[i].matematica > maior) entao
        para j de 1 ate k faca
          nomes[j] <- ""
        fimpara

        k <- 1
        maior <- aluno[i].matematica
        nomes[k] <- aluno[i].nome
      senao
        se (aluno[i].matematica = maior) entao
          k <- k + 1
          nomes[k] <- aluno[i].nome
        fimse
      fimse
    fimse

    se (aluno[i].matematica >= 60) entao
      aluno[i].situacao <- "APROVADO"
      qapv <- qapv + 1
    senao
      se (aluno[i].matematica < 40) entao
        aluno[i].situacao <- "REPROVADO"
        qrpv <- qrpv + 1
      senao
        aluno[i].situacao <- "EM RECUPERAÇÃO"
        qrec <- qrec + 1
      fimse
    fimse

    escreval
  fimpara

  para j de (k - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (maiusc(nomes[i]) > maiusc(nomes[i + 1])) entao
        aux <- nomes[i]
        nomes[i] <- nomes[i + 1]
        nomes[i + 1] <- aux
      fimse
    fimpara
  fimpara

  para i de 1 ate lsup faca
    para j de 1 ate lsupn faca
      media[j] <- media[j] + mat[i, j]
    fimpara
  fimpara

  para i de 1 ate lsupn faca
    media[i] <- media[i]/lsup

    para j de 1 ate lsup faca
      se (mat[j, i] > media[i]) entao
        qacm[i] <- qacm[i] + 1
      fimse
    fimpara
  fimpara

  escreval("Quantidade de alunos aprovados:", qapv, ".")
  escreval("Quantidade de alunos reprovados:", qrpv, ".")
  escreval("Quantidade de alunos em recuperação:", qrec, ".")
  escreval

  escreval("Maior nota final:", maior, ".")
  escreva("Aluno(s) que a conquistaram: ")

  para i de 1 ate k faca
    se (i = k) entao
      escreval(nomes[i], ".")
    senao
      escreva(nomes[i], ",")
    fimse
  fimpara

  escreval
  escreval("Nota média de cada bimestre:")
  escreval

  para i de 1 ate lsupn faca
    escreval(i, "º bimestre:", media[i]:6:2, ";", qacm[i], " alunos ficaram acima da média.")
  fimpara

Fimalgoritmo
