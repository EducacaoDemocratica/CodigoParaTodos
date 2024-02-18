# Exercício 06

[**Ver Análise**](Analise06.md)

```markdown
Algoritmo "Q6 - Repeticao"
Var
   lsup, i, qtdMaiorMedia, qtdMediaPadrao, qtdAo, qtdMediaAo: inteiro
   a1, a2, ao, menorNota, maiorNota, maiorMedia, media: real
Inicio
   lsup <- 40
   qtdMaiorMedia <- 0
   qtdMediaPadrao <- 0
   qtdAo <- 0
   qtdMediaAo <- 0
   maiorMedia <- 0
   para i de 1 ate lsup faca
      escreval("Dados do", i,"º aluno")
      escreval("ATRIBUA A NOTA 0 CASO NÃO TENHA FEITO A PROVA")
      escreval
      escreva("Insira a nota da avaliação 1: ")
      leia(a1)
      enquanto ((a1 < 0) ou (a1 > 10))faca
         escreva("Não insira uma nota negativa ou maior que 10: ")
         leia(a1)
      fimenquanto
      menorNota <- a1
      maiorNota <- a1
      escreva("Insira a nota da avaliação 2: ")
      leia(a2)
      enquanto ((a2 < 0) ou (a2 > 10))faca
         escreva("Não insira uma nota negativa ou maior que 10: ")
         leia(a2)
      fimenquanto
      se (menorNota > a2) entao
         menorNota <- a2
      fimse
      se (maiorNota < a2) entao
         maiorNota <- a2
      fimse
      escreva("Insira a nota da avaliação optativa: ")
      leia(ao)
      enquanto ((ao < 0) ou (ao > 10))faca
         escreva("Não insira uma nota negativa ou maior que 10: ")
         leia(ao)
      fimenquanto
      se (ao <> 0) entao
         qtdAo <- qtdAo + 1
         se (ao > menorNota) entao
            menorNota <- ao
         fimse
      fimse
      media <- (menorNota + maiorNota)/2
      se (media > maiorMedia) entao
         maiorMedia <- media
         qtdMaiorMedia <- 1
      senao
         se (media = maiorMedia) entao
            qtdMaiorMedia <- qtdMaiorMedia + 1
         fimse
      fimse
      se (media >= 6) entao
         se (ao <> 0) entao
            qtdMediaAo <- qtdMediaAo + 1
         senao
            qtdMediaPadrao <- qtdMediaPadrao + 1
         fimse
      fimse
      escreval("A média desse aluno é de", media, " pontos.")
      escreval
   fimpara
   escreval("Maior média:", maiorMedia)
   escreval("Alunos que tiraram a maior média:", qtdMaiorMedia)
   escreval("Alunos que não fizeram a avaliação optativa e tiveram a média maior ou igual a 6:", qtdMediaPadrao)
   escreval("Alunos que fizeram a avaliação optativa:", qtdAo)
   escreval("Alunos que fizeram a avaliação optativa e tiveram a média maior ou igual a 6:", qtdMediaAo)
Fimalgoritmo
