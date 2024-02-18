# Exercício 22

[**Ver Análise**](Analise22.md)

```markdown
Algoritmo "Q22 - Condicional"
Var
   a, b, c, d, x1, x2: real
Inicio
   escreval("Equação quadrática: ax² + bx + c = 0")
   escreval
   escreva("Insira o coeficiente a: ")
   leia(a)

   se (a = 0) entao
      escreval("A equação não é quadrática.")
   senao
      escreva("Insira b: ")
      leia(b)
      escreva("Insira c: ")
      leia(c)
      escreval
      d <- b^2 - (4*a*c)

      se (d < 0) entao
         escreval("A equação não possui raízes reais.")
      senao
         x1 <- (-b + (d^(1/2))) / (2*a)
         x2 <- (-b - (d^(1/2))) / (2*a)

         se (d = 0) entao
            escreval("A equação possui duas raízes reais iguais a ", x1)
         senao
            escreval("A equação possui duas raízes reais distintas x1 =", x1, " e x2 =", x2, ".")
         fimse
      fimse
   fimse
Fimalgoritmo
