# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown
Algoritmo "Q23 - Condicional"
Var
   ano: inteiro
Inicio
   escreva("Insira o ano: ")
   leia(ano)

   se (ano < 0) entao
      escreval("Erro: o ano inserido é negativo.")
   senao
      se ((ano mod 4 = 0) e nao(ano mod 100 = 0)) entao
         escreval("O ano é bissexto.")
      senao
         escreval("O ano não é bissexto.")
      fimse
   fimse
Fimalgoritmo
