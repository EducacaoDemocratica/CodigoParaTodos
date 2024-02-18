# Exercício 28

[**Ver Análise**](Analise28.md)

```markdown
Algoritmo "Q28 - Repeticao"
Var
   a, b, c, linf, lsup, q, i, j: inteiro
   d, x1, x2: real
Inicio
   linf <- -5
   lsup <- 2
   q <- 0

   para a de linf ate lsup faca
      se (a <> 0) entao
         para b de linf ate lsup faca
            para c de linf ate lsup faca
               d <- b^2 - (4*a*c)
               se (d >= 0) entao
                  x1 <- (-b + d ^ (1/2))/(2 * a)
                  x2 <- (-b - d ^ (1/2))/(2 * a)
                  se (x1 <> x2) entao
                     se (x1 < 0) entao
                        x1 <- -x1
                     fimse
                     se (x2 < 0) entao
                        x2 <- -x2
                     fimse
                     i <- 0
                     enquanto (i < x1) faca
                        i <- i + 1
                     fimenquanto
                     
                     j <- 0
                     enquanto (j < x2) faca
                        j <- j + 1
                     fimenquanto

                     se ((i = x1) e (j = x2)) entao
                        q <- q + 1
                        escreval(q, "ª equação: -(", b,") +- ((",b,"² - 4*",a,"*",c,")^(1/2))/(2 *",a,")")
                     fimse
                  fimse
               fimse
            fimpara
         fimpara
      fimse
   fimpara

   escreval
   escreval("Existem", q, " equações.")
Fimalgoritmo
