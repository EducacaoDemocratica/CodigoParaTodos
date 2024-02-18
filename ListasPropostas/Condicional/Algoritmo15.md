# Exercício 15

[**Ver Análise**](Analise15.md)

```markdown
Algoritmo "Q15 - Condicional"
Var
   a, b, c: real
   t: logico
Inicio
   t <- verdadeiro

   escreva("Insira o valor para um lado de um triângulo: ")
   leia(a)
   
   se (a <= 0) entao
      escreval("Não há lado negativo ou nulo em um triângulo.")
   senao
      escreva("Insira o valor para um lado: ")
      leia(b)
      
      se (b <= 0) entao
         escreval("Não há lado negativo ou nulo.")
      senao
         escreva("Insira o valor para um lado: ")
         leia(c)
         
         se (c <= 0) entao
            escreval("Não há lado negativo ou nulo.")
         senao
            escreval
            
            se ((a > (b + c)) ou (b > (a + c)) ou (c > (a + b))) entao
               t <- falso
            fimse
            
            se (t = verdadeiro) entao
               se ((a = b) e (b = c)) entao
                  escreval("O triângulo é equilátero.")
               senao
                  se ((a = c) ou (a = b) ou (b = c)) entao
                     escreval("O triângulo é isóceles.")
                  senao
                     escreval("O triângulo é escaleno.")
                  fimse
               fimse
            senao
               escreval("Os lados não podem formar um triângulo.")
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
