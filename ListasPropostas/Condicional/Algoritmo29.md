# Exercício 29

[**Ver Análise**](Analise29.md)

```markdown
Algoritmo "Q29 - Condicional"
Var
   sa, sr: real
   nome: caractere
Inicio
   escreva("Insira seu nome:")
   leia(nome)

   se (nome = "") entao
      escreval("Erro: campo vazio.")
   senao
      escreva("Insira o valor do seu salário atual: R$")
      leia(sa)

      se (sa <= 0) entao
         escreval("Erro: salário nulo ou negativo.")
      senao
         escreval

         se (sa <= 1200) entao
            sr <- (sa * 1.3)
         senao
            se (sa <= 2500) entao
               sr <- (sa * 1.2)
            senao
               sr <- (sa * 1.1)
            fimse
         fimse

         escreval("Funcionário: ", nome, ".")
         escreval("Salário antigo: R$", sa, ".")
         escreval("Salário reajustado: R$", sr, ".")
      fimse
   fimse
Fimalgoritmo
