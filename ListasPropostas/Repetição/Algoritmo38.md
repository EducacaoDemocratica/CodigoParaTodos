# Exercício 38

[**Ver Análise**](Analise38.md)

```markdown
Algoritmo "Q38 - Repeticao"
Var
   a, b, c, d, linf, lsup: inteiro
   r1, r2: real
Inicio
   linf <- 1
   lsup <- 9

   para a de linf ate lsup faca
      para b de linf ate lsup faca
         para c de linf ate lsup faca
            para d de linf ate lsup faca
               r1 <- (a^b) * (c^d)
               r2 <- a * b * c * d

               se (r1 = r2) entao
                  escreval("Resultado das expressões: ")
                  escreval
                  escreval(a, " ^", b, " *", c, " ^", d, " =", r1)
                  escreval(a, " *", b, " *", c, " *", d, " =", r2)
                  escreval
                  escreval("Algarismo A:", a)
                  escreval("Algarismo B:", b)
                  escreval("Algarismo C:", c)
                  escreval("Algarismo D:", d)
               fimse
            fimpara
         fimpara
      fimpara
   fimpara
Fimalgoritmo
