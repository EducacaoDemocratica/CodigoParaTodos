# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - Condicional"
Var
   n: inteiro
Inicio
   escreva("Insira um número: ")
   leia(n)

   se ((n mod 3 = 0) e (n mod 5 = 0)) entao
      escreval(n, " é múltiplo de 3 e 5.")
   senao
      se (n mod 3 = 0) entao
         escreval(n, " é múltiplo de 3, mas não de 5.")
      senao
         se (n mod 5 = 0) entao
            escreval(n, " é múltiplo de 5, mas não de 3.")
         senao
            escreval(n, " não é múltiplo de 3 e nem de 5.")
         fimse
      fimse
   fimse
Fimalgoritmo
