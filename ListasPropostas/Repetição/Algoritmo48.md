# Exercício 48 - Repeticao

[**Ver Análise**](Analise48.md)

```markdown
Algoritmo "Q48 - Repeticao"
Var
   lsup, i, valorComputador, valorJogador, pontosJogador, soma, aux: inteiro
   apostaComputador, apostaJogador: caracter
   pontosComputador
Inicio
   lsup <- 5
   pontosComputador <- 0
   pontosJogador <- 0

   para i de 1 ate lsup faca
      escreval(i,"ª rodada")
      escreval
      valorComputador <- randi(6)
      aux <- randi(2)
      
      se (aux mod 2 = 0) entao
         apostaComputador <- "P"
      senao
         apostaComputador <- "I"
      fimse

      escreval("Apostas do computador feitas.")
      escreval
      escreva("Insira a quantidade de números: ")
      leia(valorJogador)
      
      enquanto ((valorJogador < 0) ou (valorJogador > 5)) faca
         escreva("Coloque valores de 0 a 5: ")
         leia(valorJogador)
      fimenquanto

      escreva("Aposte (I - Ímpar; P - Par): ")
      leia(apostaJogador)
      apostaJogador <- maiusc(apostaJogador)

      enquanto ((apostaJogador = "") ou ((apostaJogador <> "I") e (apostaJogador <> "P"))) faca
         escreva("Valor inválido, insira outro: ")
         leia(apostaJogador)
         apostaJogador <- maiusc(apostaJogador)
      fimenquanto

      soma <- valorComputador + valorJogador
      escreval
      escreval("Computador: ", apostaComputador)
      escreval("Jogador: ", apostaJogador)
      escreval("Resultado:", soma)
      escreval

      se (soma mod 2 = 0) entao
         se (apostaJogador = "P") entao
            pontosJogador <- pontosJogador + 1
         fimse

         se (apostaComputador = "P") entao
            pontosComputador <- pontosComputador + 1
         fimse
      senao
         se (apostaJogador = "I") entao
            pontosJogador <- pontosJogador + 1
         fimse

         se (apostaComputador = "I") entao
            pontosComputador <- pontosComputador + 1
         fimse
      fimse
   fimpara

   escreval("Fim de jogo.")

   se (pontosComputador > pontosJogador) entao
      escreval("O computador venceu.")
   senao
      se (pontosComputador < pontosJogador) entao
         escreval("O jogador venceu.")
      senao
         escreval("Empate.")
      fimse
   fimse
Fimalgoritmo
