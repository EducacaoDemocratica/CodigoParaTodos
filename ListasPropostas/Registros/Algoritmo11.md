# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown
Algoritmo "Q11 - Registros"

Tipo TAluno = Registro
  nome: caractere
  proxIndice: inteiro
FimRegistro

Var
  alunos: vetor [1..30] de TAluno
  paux, caract: caractere
  posInicio, lsup, i, j, p, aux, tam: inteiro
  trocou: logico

Inicio
  lsup <- 30
  posInicio <- -1

  para i de 1 ate lsup faca
    escreva("Insira o nome do", i,"º aluno: ")
    leia(alunos[i].nome)
    paux <- ""
    tam <- compr(alunos[i].nome)

    para j de 1 ate tam faca
      caract <- copia(alunos[i].nome; j; 1)
      se (caract <> " ") entao
        paux <- paux + caract
    fimpara

    enquanto (paux = "") faca
      escreva("Não preencha com espaços vazios: ")
      leia(alunos[i].nome)
      paux <- ""
      tam <- compr(alunos[i].nome)

      para j de 1 ate tam faca
        caract <- copia(alunos[i].nome; j; 1)
        se (caract <> " ") entao
          paux <- paux + caract
      fimpara
    fimenquanto

    alunos[i].nome <- maiusc(paux)
    j <- 1

    enquanto (j < lsup) faca
      se (j <> i) entao
        enquanto (alunos[i].nome = alunos[j].nome) faca
          escreva("Esse nome já está cadastrado: ")
          leia (alunos[i].nome)
          paux <- ""
          tam <- compr(alunos[i].nome)

          para j de 1 ate tam faca
            caract <- copia(alunos[i].nome; j; 1)
            se (caract <> " ") entao
              paux <- paux + caract
          fimpara

          enquanto (paux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(alunos[i].nome)
            paux <- ""
            tam <- compr(alunos[i].nome)

            para j de 1 ate tam faca
              caract <- copia(alunos[i].nome; j; 1)
              se (caract <> " ") entao
                paux <- paux + caract
              fimse
            fimenquanto
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto

    se (i = 1) entao
      alunos[i].proxIndice <- -1
      posInicio <- i
    senao
      se (alunos[i].nome < alunos[posInicio].nome) entao
        alunos[i].proxIndice <- posInicio
        posInicio <- i
      senao
        p <- posInicio
        trocou := false

        repita
          enquanto ((alunos[p].proxIndice <> -1) e (not trocou)) faca
            p <- alunos[p].proxIndice

          se (alunos[p].nome > alunos[i].nome) entao
            aux := 0
            j := 0

            enquanto ((aux = 0) e (j <= i)) faca
              j := j + 1

              se (alunos[j].proxIndice = p) entao
                aux := j
              fimse
            fimenquanto

            alunos[aux].proxIndice := i
            alunos[i].proxIndice := p
            trocou := true
          fimse
        ate (trocou)

        se (not trocou) entao
          alunos[i].proxIndice := -1
          alunos[p].proxIndice := i
        fimse
      fimse
    fimse
  fimenquanto

  escreval
  escreval(" 1º aluno: ", alunos[posInicio].nome,".")
  j := 1
  p := alunos[posInicio].proxIndice

  enquanto (p <> -1) faca
    j := j + 1
    escreval(j,"º aluno: ", alunos[p].nome,".")
    p := alunos[p].proxIndice
  fimenquanto

Fimalgoritmo
