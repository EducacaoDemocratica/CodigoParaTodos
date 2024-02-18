# Exercício 38

[**Ver Análise**](Analise38.md)

```markdown
Algoritmo "Q38 - Condicional"
Var
   n: real
   c, nome: caractere
Inicio
   escreva("Insira seu nome: ")
   leia(nome)

   se (nome = "") entao
      escreval("Erro: campo vazio.")
   senao
      escreva("Insira sua nota: ")
      leia(n)

      se ((n < 0) ou (n > 10)) entao
         escreval("Erro: nota negativa ou maior que 10 inserida.")
      senao
         se (n < 4) entao
            c <- "E"
         senao
            se (n < 6) entao
               c <- "D"
            senao
               se (n < 7.5) entao
                  c <- "C"
               senao
                  se (n < 8.5) entao
                     c <- "B"
                  senao
                     c <- "A"
                  fimse
               fimse
            fimse
         fimse
      fimse

      escreval
      escreval("Nome: ", nome,".")
      escreval("Nota:", n,".")
      escreval("Conceito: ", c,".")
   fimse
Fimalgoritmo
