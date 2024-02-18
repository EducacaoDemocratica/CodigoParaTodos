# Exercício 39

[**Ver Análise**](Analise39.md)

```markdown
Algoritmo "Q39 - Condicional"
Var
   nome, c1, c2, c3, c4, c5, c6, min, max, s: caractere
Inicio
   escreva("Insira seu nome: ")
   leia(nome)

   se (nome = "") entao
      escreval("Erro: campo vazio.")
   senao
      escreva("Insira o 1º conceito: ")
      leia(c1)
      c1 <- maiusc(c1)
      se ((c1 <> "A") e (c1 <> "B") e (c1 <> "C") e (c1 <> "D") e (c1 <> "E")) entao
         escreval("Erro: conceito inválido inserido.")
      senao
         max <- c1
         min <- c1

         escreva("Insira o 2º conceito: ")
         leia(c2)
         c2 <- maiusc(c2)
         se ((c2 <> "A") e (c2 <> "B") e (c2 <> "C") e (c2 <> "D") e (c2 <> "E")) entao
            escreval("Erro: conceito inválido inserido.")
         senao
            se (c2 < max) entao
               max <- c2
            fimse
            se (c2 > min) entao
               min <- c2
            fimse

            escreva("Insira o 3º conceito: ")
            leia(c3)
            c3 <- maiusc(c3)
            se ((c3 <> "A") e (c3 <> "B") e (c3 <> "C") e (c3 <> "D") e (c3 <> "E")) entao
               escreval("Erro: conceito inválido inserido.")
            senao
               se (c3 < max) entao
                  max <- c3
               fimse
               se (c3 > min) entao
                  min <- c3
               fimse

               escreva("Insira o 4º conceito: ")
               leia(c4)
               c4 <- maiusc(c4)
               se ((c4 <> "A") e (c4 <> "B") e (c4 <> "C") e (c4 <> "D") e (c4 <> "E")) entao
                  escreval("Erro: conceito inválido inserido.")
               senao
                  se (c4 < max) entao
                     max <- c4
                  fimse
                  se (c4 > min) entao
                     min <- c4
                  fimse

                  escreva("Insira o 5º conceito: ")
                  leia(c5)
                  c5 <- maiusc(c5)
                  se ((c5 <> "A") e (c5 <> "B") e (c5 <> "C") e (c5 <> "D") e (c5 <> "E")) entao
                     escreval("Erro: conceito inválido inserido.")
                  senao
                     se (c5 < max) entao
                        max <- c5
                     fimse
                     se (c5 > min) entao
                        min <- c5
                     fimse

                     escreva("Insira o 6º conceito: ")
                     leia(c6)
                     c6 <- maiusc(c6)
                     se ((c6 <> "A") e (c6 <> "B") e (c6 <> "C") e (c6 <> "D") e (c6 <> "E")) entao
                        escreval("Erro: conceito inválido inserido.")
                     senao
                        se (c6 < max) entao
                           max <- c6
                        fimse
                        se (c6 > min) entao
                           min <- c6
                        fimse

                        escreval
                        se (min = "E") entao
                           s <- "Reprovado."
                        senao
                           se (((min = "D") e (max = "B")) ou ((min = "C") e (max = "C"))) entao
                              s <- "Em recuperação."
                           senao
                              s <- "Aprovado."
                           fimse
                        fimse

                        escreval("Nome: ", nome)
                        escreval("Maior conceito: ", max)
                        escreval("Menor conceito: ", min)
                        escreval("Situação final: ", s)
                     fimse
                  fimse
               fimse
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
