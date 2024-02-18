# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown
Algoritmo "Q17 - Condicional"
Var
   a, b, c: real
Inicio
   escreva("Insira a medida de um cateto: ")
   leia(b)
   
   se (b <= 0) entao
      escreval("Não há cateto negativo ou nulo em um triângulo.")
   senao
      escreva("Insira a medida de um cateto: ")
      leia(c)
      
      se (c <= 0) entao
         escreval("Não há cateto negativo ou nulo.")
      senao
         escreval
         
         a <- (((b^2) + (c^2))^(1/2))
         escreval("A medida da hipotenusa é", a,".")
      fimse
   fimse
Fimalgoritmo
