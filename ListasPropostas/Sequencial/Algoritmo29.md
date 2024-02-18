# Exercício 29

[**Ver Análise**](Analise29.md)

```markdown
Algoritmo "Q29 - Sequencial"
Var
   km: inteiro
   qlitro, pgas, ggas, t, gtotal: real
Inicio
   escreva("Insira a distância a ser percorrida (em km): ")
   leia(km)
   escreva("Insira o valor do litro de gasolina: R$")
   leia(pgas)
   escreval
   qlitro <- km/11
   ggas <- pgas * qlitro
   t <- ggas * 0.45
   gtotal <- ggas + t
   escreval("Combustível necessário:", qlitro:6:2, " litro(s).")
   escreval("Gasto com gasolina: R$", ggas:6:2, ".")
   escreval("Taxa do motorista: R$", t:6:2, ".")
   escreval("Gasto total: R$", gtotal:6:2, ".")
Fimalgoritmo
