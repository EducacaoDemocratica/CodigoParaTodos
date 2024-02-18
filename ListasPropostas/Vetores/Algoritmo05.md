# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - Vetor"
Var
  i, lsup, q, menor, maior: inteiro
  t: vetor [1..121] de inteiro
  m: real

Inicio
  lsup <- 10
  m <- 0
  q <- 0

  para i de 1 ate lsup faca
    escreva("Insira a temperatura do ", i, "º dia: ")
    leia(t[i])

    enquanto ((t[i] < 15) ou (t[i] > 40)) faca
      escreva("A temperatura deve estar entre 15ºC e 40ºC: ")
      leia(t[i])
    fimenquanto
  fimpara

  para i de 1 ate lsup faca
    se (i = 1) entao
      maior <- t[i]
      menor <- t[i]
    senao
      se (t[i] > maior) entao
        maior <- t[i]
      fimse

      se (t[i] < menor) entao
        menor <- t[i]
      fimse
    fimse

    m <- m + t[i]
  fimpara

  m <- m/i

  para i de 1 ate lsup faca
    se (t[i] < m) entao
      q <- q + 1
    fimse
  fimpara

  escreval
  escreval("Menor temperatura registrada: ", menor, "ºC.")
  escreval("Maior temperatura registrada: ", maior, "ºC.")
  escreval("Temperatura média: ", m, "ºC.")
  escreval("Nº de dias em que a temperatura foi menor que a média: ", q, " dias.")

Fimalgoritmo
