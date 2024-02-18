# Exercício 34

[**Ver Análise**](Analise34.md)

```markdown
Algoritmo "Q34 - Condicional"
Var
   p, ml, g: real
   mg: inteiro
Inicio
   escreva("Insira seu peso: ")
   leia(p)

   se (p <= 0) entao
      escreval("Erro: peso nulo ou negativo encontrado.")
   senao
      escreval

      se (p <= 9) entao
         mg <- 100
      senao
         se (p <= 16) entao
            mg <- 250
         senao
            se (p <= 24) entao
               mg <- 350
            senao
               se (p <= 30) entao
                  mg <- 500
               senao
                  mg <- 750
               fimse
            fimse
         fimse
      fimse

      ml <- (mg/500)
      g <- ml * 10

      escreval("Peso:", p, "kg.")
      escreval("Dosagem:", mg, "mg/", ml, "ml.")
      escreval("Gotas:", g, ".")
   fimse
Fimalgoritmo
