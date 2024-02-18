# Exercício 33

[**Ver Análise**](Analise33.md)

```markdown
Algoritmo "Q33 - Sequencial"
Var
   sbruto, sliquido, prev, fg: real
Inicio
   escreva("Insira o valor do salário bruto: R$")
   leia(sbruto)
   escreval
   sliquido <- sbruto
   prev <- sliquido * (8/100)
   sliquido <- sliquido - prev
   fg <- sliquido * (12/100)
   sliquido <- sliquido - fg
   escreval("Salário bruto: R$", sbruto:6:2, ".")
   escreval("Desconto da previdência social: R$", prev:6:2, ".")
   escreval("Desconto do fundo de garantia: R$", fg:6:2, ".")
   escreval("Salário líquido: R$", sliquido:6:2, ".")
Fimalgoritmo
