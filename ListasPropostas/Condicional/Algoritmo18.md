# Exercício 18

[**Ver Análise**](Analise18.md)

```markdown
Algoritmo "Q18 - Condicional"
Var
   l1, l2, l3, a, c, b: inteiro
   t: logico
Inicio
   t <- verdadeiro
   escreva("Insira o valor para um lado de um triângulo: ")
   leia(l1)
   
   se (l1 <= 0) entao
      escreval("Não há lado negativo ou nulo em um triângulo.")
   senao
      escreva("Insira o valor para um lado: ")
      leia(l2)
      
      se (l2 <= 0) entao
         escreval("Não há lado negativo ou nulo.")
      senao
         escreva("Insira o valor para um lado: ")
         leia(l3)
         
         se (l3 <= 0) entao
            escreval("Não há lado negativo ou nulo.")
         senao
            escreval
            
            se ((l1 > (l2 + l3)) ou (l2 > (l1 + l3)) ou (l3 > (l1 + l2))) entao
               t <- falso
            fimse
            
            se (t = verdadeiro) entao
               se ((l1 > l2) e (l1 > l3)) entao
                  a <- l1
                  b <- l2
                  c <- l3
               senao
                  se ((l2 > l1) e (l2 > l3)) entao
                     a <- l2
                     b <- l1
                     c <- l3
                  senao
                     a <- l3
                     b <- l1
                     c <- l2
                  fimse
               fimse
               
               se ((a^2) = ((b^2) + (c^2))) entao
                  escreval("O triângulo é retângulo.")
               senao
                  se ((a^2) > ((b^2) + (c^2))) entao
                     escreval("O triângulo é obtusângulo.")
                  senao
                     escreval("O triângulo é acutângulo.")
                  fimse
               fimse
            senao
               escreval("Os lados não podem formar um triângulo.")
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
