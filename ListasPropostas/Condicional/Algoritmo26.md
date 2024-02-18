# Exercício 26

[**Ver Análise**](Analise26.md)

```markdown
Algoritmo "Q26 - Condicional"
Var
   p, f, t, cem, cinq, v, d, c, um: inteiro
Inicio
   cem <- 0
   cinq <- 0
   v <- 0
   d <- 0
   c <- 0
   um <- 0

   escreva("Insira o valor do produto: R$")
   leia(p)

   se (p <= 0) entao
      escreval("Erro: valor inválido.")
   senao
      escreva("Insira o valor fornecido pelo cliente: R$")
      leia(f)

      se (f <= 0) entao
         escreval("Erro: valor inválido.")
      senao
         escreval
         escreval("Valor do produto: R$", p, ".")
         escreval("Valor pago pelo cliente: R$", f, ".")

         se (f >= p) entao
            t <- f - p
            escreval("Valor do troco: R$", t, ".")

            se (t > 0) entao
               cem <- t div 100
               t <- t - (cem * 100)
               cinq <- t div 50
               t <- t - (cinq * 50)
               v <- t div 20
               t <- t - (v * 20)
               d <- t div 10
               t <- t - (d * 10)
               c <- t div 5
               t <- t - (c * 5)
               um <- t

               escreval(cem, " cédula(s) de R$100.")
               escreval(cinq, " cédula(s) de R$50.")
               escreval(v, " cédula(s) de R$20.")
               escreval(d, " cédula(s) de R$10.")
               escreval(c, " cédula(s) de R$5.")
               escreval(um, " cédula(s) de R$1.")
            fimse
         senao
            escreval("Não há troco a ser devolvido.")
         fimse
      fimse
   fimse
Fimalgoritmo
