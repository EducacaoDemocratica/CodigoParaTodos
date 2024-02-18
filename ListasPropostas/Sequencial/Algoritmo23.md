# Exercício 23

[**Ver Análise**](Analise23.md)

```markdown
Algoritmo "Q23 - Sequencial"
Var
   a1, an, n: inteiro
   sn: real
Inicio
   escreva("Insira o valor do primeiro termo (a1): ")
   leia(a1)
   escreva("Insira o valor do último termo (an): ")
   leia(an)
   escreva("Insira a quantidade de números de", a1," até", an,": ")
   leia(n)
   escreval
   sn <- ((a1 + an) * n)/2
   escreval("A soma dos", n, " números da sequência", a1, " a", an, " é", sn, ".")
Fimalgoritmo
