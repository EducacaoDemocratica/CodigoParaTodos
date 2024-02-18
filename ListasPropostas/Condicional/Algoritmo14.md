# Exercício 14

[**Ver Análise**](Analise14.md)

```markdown
Algoritmo "Q14 - Condicional"
Var
   l1, l2, l3: real
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
               escreval("Os lados podem formar um triângulo.")
            senao
               escreval("Os lados não podem formar um triângulo.")
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
