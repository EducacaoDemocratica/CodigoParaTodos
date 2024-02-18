# Exercício 19

[**Ver Análise**](Analise19.md)

```markdown
Algoritmo "Q19 - Sequencial"
Var
   v, v0, a, d: real
Inicio
   escreva("Insira a velocidade inicial do corpo (m/s): ")
   leia(v0)
   escreva("Insira a aceleração (m/s²): ")
   leia(a)
   escreva("Insira a distância percorrida (d): ")
   leia(d)
   escreval
   v <- (v0 ^ 2 + 2 * a * d)^(1/2)
   escreval("A velocidade final é", v:6:2, "m/s.")
Fimalgoritmo
