# Exercício 30

[**Ver Análise**](Analise30.md)

```markdown
Algoritmo "Q30 - Condicional"
Var
   a, p: real
   s: caracter
Inicio
   escreva("Insira o seu sexo (M - Masculino, F - Feminino): ")
   leia(s)
   s <- maiusc(s)

   se ((s <> "M") e (s <> "F")) entao
      escreval("Erro: o código do sexo inserido é inválido.")
   senao
      escreva("Insira a altura: ")
      leia(a)

      se (a <= 0) entao
         escreval("Erro: altura negativa ou nula lida.")
      senao
         escreval

         se (s = "M") entao
            p <- (72.7 * a) – 58
         senao
            p <- (62.1 * a) - 44.7
         fimse

         escreval("Seu peso ideal é ", p, "kg.")
      fimse
   fimse
Fimalgoritmo
