# Exercício 36

[**Ver Análise**](Analise36.md)

```markdown
Algoritmo "Q36 - Condicional"
Var
   p, b, s, cal: inteiro
Inicio
   cal <- 0

   escreval("
   PRATO
   | SOBREMESA
   | BEBIDA")
   escreval
   escreval("0: Nenhum")
   escreval("1: Vegetariano | Abacaxi | Chá")
   escreval("2: Peixe | Sorvete diet | Suco de laranja")
   escreval("3: Frango | Mousse diet | Suco de melão")
   escreval("4: Carne | Mouse de chocolate | Refrigerante diet")
   escreval

   escreva("Qual o prato escolhido? ")
   leia(p)

   se ((p < 0) ou (p > 4)) entao
      escreval("Erro, o código digitado não está no cardápio.")
   senao
      se (p = 0) entao
         cal <- cal + 0
      senao
         se (p = 1) entao
            cal <- cal + 180
         senao
            se (p = 2) entao
               cal <- cal + 230
            senao
               se (p = 3) entao
                  cal <- cal + 250
               senao
                  cal <- cal + 350
               fimse
            fimse
         fimse
      fimse
   fimse

   escreva("Qual a sobremesa escolhida? ")
   leia(s)

   se ((s < 0) ou (s > 4)) entao
      escreval("Erro, o código digitado não está no cardápio.")
   senao
      se (s = 0) entao
         cal <- cal + 0
      senao
         se (s = 1) entao
            cal <- cal + 75
         senao
            se (s = 2) entao
               cal <- cal + 110
            senao
               se (s = 3) entao
                  cal <- cal + 170
               senao
                  cal <- cal + 200
               fimse
            fimse
         fimse
      fimse
   fimse

   escreva("Qual a bebida escolhida? ")
   leia(b)

   se ((b < 0) ou (b > 4)) entao
      escreval("Erro, o código digitado não está no cardápio.")
   senao
      se (b = 0) entao
         cal <- cal + 0
      senao
         se (b = 1) entao
            cal <- cal + 20
         senao
            se (b = 2) entao
               cal <- cal + 70
            senao
               se (b = 3) entao
                  cal <- cal + 100
               senao
                  cal <- cal + 65
               fimse
            fimse
         fimse
      fimse
   fimse

   escreval("Total de calorias consumidas:", cal,"cal.")
Fimalgoritmo
