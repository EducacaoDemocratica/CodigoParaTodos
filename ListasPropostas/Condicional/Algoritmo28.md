# Exercício 28

[**Ver Análise**](Analise28.md)

```markdown
Algoritmo "Q28 - Condicional"
Var
   valorComputador, valorJogador, soma, apostaComputador, apostaJogador: inteiro
Inicio
   valorComputador <- randi(6)
   apostaComputador <- randi(6) + valorComputador

   escreval("Apostas do computador feitas.")
   escreval

   escreva("Insira a quantidade de palitinhos: ")
   leia(valorJogador)

   se ((valorJogador < 0) ou (valorJogador > 5)) entao
      escreval("Erro: quantidade negativa ou maior que 5 encontrada.")
   senao
      escreva("Aposte o valor da soma dos palitinhos: ")
      leia(apostaJogador)

      se ((apostaJogador < 0) ou (apostaJogador > 10)) entao
         escreval("Erro: quantidade negativa ou maior que 10 encontrada.")
      senao
         soma <- valorComputador + valorJogador

         escreval
         escreval("Palitinhos do computador: ", valorComputador)
         escreval("Palitinhos do jogador: ", valorJogador)
         escreval("Soma:", soma)
         escreval
         escreval("Aposta do computador: ", apostaComputador)
         escreval("Aposta do jogador: ", apostaJogador)
         escreval
         escreva("Resultado: ")

         se (apostaComputador = apostaJogador) entao
            escreval("empate.")
         senao
            se (apostaJogador = soma) entao
               escreval("o usuário venceu.")
            senao
               se (apostaComputador = soma) entao
                  escreval("o computador venceu.")
               senao
                  escreval("empate.")
               fimse
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
