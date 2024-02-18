# Exercício 46 - Repetição

[**Ver Análise**](Analise46.md)

```markdown
Algoritmo "Q46 - Repeticao"
Var
   i, n, k, aux1, aux2, aux3: inteiro
   fat, num, s: real
Inicio
   aux1 <- 0
   aux2 <- 1
   escreva("Insira o valor de n: ")
   leia(n)
   
   enquanto (n <= 0) faca
      escreva("n deve ser maior que zero: ")
      leia(n)
   fimenquanto
   
   escreval
   para i de 1 ate n faca
      aux3 <- aux1 + aux2
      aux1 <- aux2
      aux2 <- aux3
      k <- 0
      fat <- 1
      
      enquanto (k < i) faca
         k <- k + 1
         fat <- fat * k
      fimenquanto
      
      se (i mod 2 = 0) entao
         s <- s - aux1/fat
      senao
         s <- s + aux1/fat
      fimse
   fimpara

   escreval("O valor de s com", n, " números é", s)
Fimalgoritmo
