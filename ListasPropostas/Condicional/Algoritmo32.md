# Exercício 32

[**Ver Análise**](Analise32.md)

```markdown
Algoritmo "Q32 - Condicional"
Var
   a1, a2, ao, menor, maior, m: real
Inicio
   escreval("Insira 0 caso não tenha realizado alguma prova.")
   escreval("Valor máximo de nota: 10")
   escreval

   escreva("Qual sua nota na prova 1? ")
   leia(a1)

   se ((a1 < 0) ou (a1 > 10)) entao
      escreval("Valor inválido inserido.")
   senao
      escreva("Qual sua nota na prova 2? ")
      leia(a2)

      se ((a2 < 0) ou (a2 > 10)) entao
         escreval("Valor inválido inserido.")
      senao
         se (a1 > a2) entao
            menor <- a2
            maior <- a1
         senao
            menor <- a1
            maior <- a2
         fimse

         escreva("Qual sua nota na prova opcional? ")
         leia(ao)

         se ((ao < 0) ou (ao > 10)) entao
            escreval("Valor inválido inserido.")
         senao
            se (ao <> 0) e (ao > menor) entao
               menor <- ao
            fimse

            m <- ((maior + menor) / 2)
            escreval
            escreval("Média do aluno: ", m, ".")

            se (m < 4) entao
               escreval("O aluno está reprovado.")
            senao
               se (m < 6) entao
                  escreval("O aluno está em recuperação.")
               senao
                  escreval("O aluno está aprovado.")
               fimse
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
