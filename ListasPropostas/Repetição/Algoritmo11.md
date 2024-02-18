# Exercício 11

[**Ver Análise**](Analise11.md)

```markdown
Algoritmo "Q11 - Repeticao"
Var
   n, contaTernos: inteiro
   i, j, k, i2, j2, k2, i0: inteiro
Inicio
   contaTernos <- 0
   i0 <- 0
   i <- 1
   j <- 1
   k <- 1
   escreva("Insira a quantidade de ternos: ")
   leia(n)
   
   enquanto (n <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(n)
   fimenquanto
   
   escreval
   
   enquanto (contaTernos < n) faca
      para j de 1 ate i faca
         para k de 1 ate i faca
            i2 <- i * i
            j2 <- j * j
            k2 <- k * k
            
            se ((i2 = j2 + k2) e (contaTernos < n) e (i0 <> i)) entao
               contaTernos <- contaTernos + 1
               i0 <- i
               escreva(contaTernos,"º terno: ", i,",", j,",", k,".")
               escreval
            fimse
         fimpara
      fimpara
      i <- i + 1
   fimenquanto
Fimalgoritmo
