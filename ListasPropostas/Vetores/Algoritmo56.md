# Exercício 56

[**Ver Análise**](Analise56.md)

```markdown
Algoritmo "Q56 - Vetor"
var
  c: vetor [1..100] de caractere
  frase: caractere
  tamanho, i, vaziovezes, avezes: inteiro

inicio
  vaziovezes <- 0
  avezes <- 0

  escreval("Insira uma frase de até 100 caracteres: ")
  leia (frase)
  tamanho <- compr(frase)

  enquanto ((tamanho = 0) ou (tamanho > 100)) faca
    se (tamanho = 0) entao
      escreval("Preencha a frase: ")
    senao
      escreval("Essa frase tem mais de 100 caracteres. Insira outra: ")
    fimse
    leia (frase)
    tamanho <- compr(frase)
  fimenquanto

  frase <- minusc(frase)

  para i de 1 ate tamanho faca
    c[i] <- copia(frase; i; 1)

    se (c[i] = "a") entao
      avezes <- avezes + 1
    fimse

    se (c[i] = " ") entao
      vaziovezes <- vaziovezes + 1
    fimse
  fimpara

  escreval
  escreval("Existem", vaziovezes," espaços em branco na frase.")
  escreval("Existem", avezes," letras a na frase.")
Fimalgoritmo
