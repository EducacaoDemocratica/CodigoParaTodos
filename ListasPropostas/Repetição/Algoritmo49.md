# Exercício 49

[**Ver Análise**](Analise49.md)

```markdown
Algoritmo "Q49 - Repeticao"
Var
   lsup, i, valorComputador, valorJogador, pontosJogador: inteiro
   escolhaComputador, escolhaJogador: caracter
   pontosComputador
Inicio
   lsup <- 5
   pontosComputador <- 0
   pontosJogador <- 0

   para i de 1 ate lsup faca
      escreval(i,"ª rodada")
      escreval
      valorComputador <- randi(3)

      se (valorComputador = 0) entao
         escolhaComputador <- "Pedra"
      senao
         se (valorComputador = 1) entao
            escolhaComputador <- "Papel"
         senao
            escolhaComputador <- "Tesoura"
         fimse
      fimse

      escreval("Aposta do computador feita.")
      escreva("Selecione (0 - Pedra; 1 - Papel; 2 - Tesoura): ")
      leia(valorJogador)

      enquanto ((valorJogador < 0) ou (valorJogador > 2)) faca
         escreva("Selecione apenas os valores 0, 1 ou 2: ")
         leia(valorJogador)
      fimenquanto

      se (valorJogador = 0) entao
         escolhaJogador <- "Pedra"
      senao
         se (valorJogador = 1) entao
            escolhaJogador <- "Papel"
         senao
            escolhaJogador <- "Tesoura"
         fimse
      fimse

      escreval
      escreval("Computador: ", escolhaComputador)
      escreval("Jogador: ", escolhaJogador)
      escreval

      se (escolhaComputador <> escolhaJogador) entao
         se ((escolhaComputador = "Pedra") e (escolhaJogador = "Tesoura")) entao
            pontosComputador <- pontosComputador + 1
         senao
            se ((escolhaComputador = "Tesoura") e (escolhaJogador = "Papel")) entao
               pontosComputador <- pontosComputador + 1
            senao
               se ((escolhaComputador = "Papel") e (escolhaJogador = "Pedra")) entao
                  pontosComputador <- pontosComputador + 1
               senao
                  pontosJogador <- pontosJogador + 1
               fimse
            fimse
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
