# Exercício 36

[**Ver Análise**](Analise36.md)

```markdown
Algoritmo "Q36 - Sequencial"
Var
   cd, cc, t, b, i, vf: real
Inicio
   escreva("Insira o custo de disponibilidade: R$")
   leia(cd)
   escreva("Insira o custo do consumo real: R$")
   leia(cc)
   escreva("Insira a taxa fixa de iluminação: R$")
   leia(t)
   escreva("Insira o custo da bandeira vigente: R$")
   leia(b)
   escreval
   i <- cc * (34/100)
   vf <- cd + cc + t + b + i
   escreval("Disponibilidade: R$", cd, ".")
   escreval("Consumo: R$", cc, ".")
   escreval("Iluminação pública: R$", t, ".")
   escreval("Bandeira: R$", b, ".")
   escreval("Imposto sobre o consumo: R$", i, ".")
   escreval
   escreval("Valor total da conta: R$", vf, ".")
Fimalgoritmo
