# Exercício 02

[**Ver Análise**](Analise02.md)

```markdown
Algoritmo "Q2 - Condicional"
Var
   n1, n2, n3, maior, menor, inter: real
Inicio
   escreva("Insira um número: ")
   leia(n1)
   maior <- n1
   menor <- n1
   escreva("Insira um número: ")
   leia(n2)
   inter <- n2
   se (n2 > maior) entao
      maior <- n2
   fimse
   se (n2 < menor) entao
      menor <- n2
   fimse
   escreva("Insira um número: ")
   leia(n3)
   se (n3 < maior) e (n3 >= menor) entao
      inter <- n3
   senao
      se (n3 > maior) entao
         inter <- maior
         maior <- n3
      fimse
      se (n3 < menor) entao
         inter <- menor
         menor <- n3
      fimse
   fimse
   escreval
   se ((n1 = n2) e (n1 = n3)) entao
      escreval("Os números são iguais, não há ordem crescente.")
   senao
      escreval("Ordem crescente:", menor,",", inter,",", maior,".")
   fimse
Fimalgoritmo
