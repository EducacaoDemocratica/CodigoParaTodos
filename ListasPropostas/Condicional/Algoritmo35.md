# Exercício 35

[**Ver Análise**](Analise35.md)

```markdown
Algoritmo "Q35 - Condicional"
Var
   i, m: inteiro
   s: caracter
Inicio
   escreva("Insira sua idade: ")
   leia(i)

   se (i < 0) entao
      escreva("Erro: idade negativa encontrada.")
   senao
      escreva("Insira seu sexo (F - Feminino, M - Masculino): ")
      leia(s)
      escreval

      s <- maiusc(s)

      se ((s <> "F") e (s <> "M")) entao
         escreval("Erro: código não encontrado.")
      senao
         se (s = "F") entao
            se (i < 6) entao
               m <- 100
            senao
               se (i < 11) entao
                  m <- 150
               senao
                  se (i < 16) entao
                     m <- 180
                  senao
                     se (i <= 35) entao
                        m <- 210
                     senao
                        m <- 200
                     fimse
                  fimse
               fimse
            fimse
         senao
            se (i < 6) entao
               m <- 130
            senao
               se (i < 11) entao
                  m <- 150
               senao
                  se (i < 26) entao
                     m <- 180
                  senao
                     se (i <= 35) entao
                        m <- 200
                     senao
                        m <- 230
                     fimse
                  fimse
               fimse
            fimse
         fimse

         escreval("O valor de sua mensalidade é R$", m, ".")
      fimse
   fimse
Fimalgoritmo
