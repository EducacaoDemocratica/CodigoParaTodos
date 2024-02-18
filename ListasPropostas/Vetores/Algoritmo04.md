# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - Vetor"
Var
  i, lsup, nm: inteiro
  h: vetor [1..50] de real
  s: vetor [1..50] de caractere
  mt, mm, menor, maior: real

Inicio
  lsup <- 10
  mm <- 0
  mt <- 0
  nm <- 0

  escreval("Insira a altura em metros.")
  escreval

  para i de 1 ate lsup faca
    escreva("Insira a altura do ", i, "º atleta: ")
    leia(h[i])

    enquanto (h[i] <= 0) faca
      escreva("A altura deve ser maior que 0: ")
      leia(h[i])
    fimenquanto

    escreva("Insira o sexo do aluno (F - Feminino; M - Masculino): ")
    leia(s[i])
    s[i] <- maiusc(s[i])

    enquanto ((s[i] = "") ou ((s[i] <> "F") e (s[i] <> "M"))) faca
      escreva("Não preencha com espaços vazios ou diferentes de 'F'/'M': ")
      leia(s[i])
      s[i] <- maiusc(s[i])
    fimenquanto

  fimpara

  para i de 1 ate lsup faca
    se (i = 1) entao
      maior <- h[i]
      menor <- h[i]
    senao
      se (h[i] > maior) entao
        maior <- h[i]
      fimse

      se (h[i] < menor) entao
        menor <- h[i]
      fimse
    fimse

    se (s[i] = "F") entao
      nm <- nm + 1
      mm <- mm + h[i]
    fimse

    mt <- mt + h[i]
  fimpara

  mt <- mt/i

  se (nm <> 0) entao
    mm <- mm/nm
  fimse

  escreval
  escreval("Menor altura da turma: ", menor:6:2, "m.")
  escreval("Maior altura da turma: ", maior:6:2, "m.")
  escreval("Média da turma: ", mt:6:2, "m.")
  escreval("Média das mulheres: ", mm:6:2, "m.")
  escreval

  escreval("Altura das mulheres que ficaram acima da média feminina: ")
  escreval

  para i de 1 ate lsup faca
    se ((s[i] = "F") e (h[i] > mm)) entao
      escreval(h[i]:6:2, "m.")
    fimse
  fimpara

  escreval
  escreval("Altura dos estudantes que ficaram abaixo da média da turma: ")
  escreval

  para i de 1 ate lsup faca
    se (h[i] < mt) entao
      escreval(h[i]:6:2, "m.")
    fimse
  fimpara

Fimalgoritmo
