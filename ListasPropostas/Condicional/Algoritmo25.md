# Exercício 25

[**Ver Análise**](Analise25.md)

```markdown
Algoritmo "Q25 - Condicional"
Var
   h1, h2, m1, m2, p1, p2, s1, s2: inteiro
Inicio
   escreval("A idade dos(as) homens/mulheres deve ser diferente entre si.")
   escreval
   escreva("Insira a idade do 1º homem: ")
   leia(h1)

   se (h1 <= 0) entao
      escreval("Erro: idade nula ou negativa encontrada.")
   senao
      escreva("Insira a idade do 2º homem: ")
      leia(h2)

      se (h2 <= 0) entao
         escreval("Erro: idade nula ou negativa encontrada.")
      senao
         se (h2 = h1) entao
            escreval("As idades dos homens são iguais, fim do programa.")
         senao
            se (h1 > h2) entao
               s1 <- h1
               p1 <- h2
            senao
               s1 <- h2
               p1 <- h1
            fimse

            escreva("Insira a idade da 1ª mulher: ")
            leia(m1)

            se (m1 <= 0) entao
               escreval("Erro: idade nula ou negativa encontrada.")
            senao
               escreva("Insira a idade da 2ª mulher: ")
               leia(m2)

               se (m2 <= 0) entao
                  escreval("Erro: idade nula ou negativa encontrada.")
               senao
                  se (m2 = m1) entao
                     escreval("As idades das mulheres são iguais, fim do programa.")
                  senao
                     se (m1 > m2) entao
                        s2 <- m2
                        p2 <- m1
                     senao
                        s2 <- m1
                        p2 <- m2
                     fimse

                     escreval("Soma das idades do homem mais velho com a mulher mais nova:", s1 + s2)
                     escreval("Produto das idades do homem mais novo com a mulher mais velha:", p1 * p2)
                  fimse
               fimse
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
