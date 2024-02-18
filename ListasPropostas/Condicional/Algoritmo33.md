# Exercício 33

[**Ver Análise**](Analise33.md)

```markdown
Algoritmo "Q33 - Condicional"
Var
   p, a, imc: real
   s: caractere
Inicio
   escreva("Insira seu nome: ")
   leia(nome)

   se (nome = "") entao
      escreval("Erro: campo vazio")
   senao
      escreva("Insira seu peso:")
      leia(p)

      se (p <= 0) entao
         escreval("Erro: peso nulo ou negativo.")
      senao
         escreva("Insira sua altura: ")
         leia(a)

         se (a <= 0) entao
            escreval("Erro: altura nula ou negativa.")
         senao
            escreval

            imc <- p/(a^2)

            se (imc < 20) entao
               s <- "Abaixo do peso"
            senao
               se (imc <= 25) entao
                  s <- "Normal"
               senao
                  se (imc <= 30) entao
                     s <- "Sobrepeso"
                  senao
                     se (imc <= 35) entao
                        s <- "Obesidade"
                     senao
                        s <- "Obesidade mórbida"
                     fimse
                  fimse
               fimse
            fimse

            escreval("Peso: ", p, "kg.")
            escreval("Altura: ", a, "m.")
            escreval("IMC: ", imc:6:2, ".")
            escreval("Situação: ", s, ".")
         fimse
      fimse
   fimse
Fimalgoritmo
