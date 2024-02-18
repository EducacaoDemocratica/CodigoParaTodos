# Exercício 16

[**Ver Análise**](Analise16.md)

```markdown
Algoritmo "Q16 - Condicional"
Var
   l1, l2, l3, a1, a2, a3, maior: real
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
               escreval("Agora insira as medidas dos ângulos. ")
               escreva("Insira o 1º ângulo: ")
               leia(a1)
               
               se (a1 <= 0) entao
                  escreval("Não há ângulo negativo ou nulo em um triângulo.")
               senao
                  maior <- a1
                  escreva("2º ângulo: ")
                  leia(a2)
                  
                  se (a2 <= 0) entao
                     escreval("Não há ângulo negativo ou nulo.")
                  senao
                     se (a2 > maior) entao
                        maior <- a2
                     fimse
                     
                     escreva("3º ângulo: ")
                     leia(a3)
                     
                     se (a3 <= 0) entao
                        escreval("Não há ângulo negativo ou nulo.")
                     senao
                        se (a3 > maior) entao
                           maior <- a3
                        fimse
                        
                        se ((a1 + a2 + a3) <> 180) entao
                           escreval("Erro: a soma dos ângulos não é 180.")
                        senao
                           se (maior = 90) entao
                              escreval("O triângulo é retângulo.")
                           senao
                              se (maior > 90) entao
                                 escreval("O triângulo é obtusângulo.")
                              senao
                                 escreval("O triângulo é actuângulo.")
                              fimse
                           fimse
                        fimse
                     fimse
                  fimse
               fimse
            senao
               escreval("Os lados não podem formar um triângulo.")
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
