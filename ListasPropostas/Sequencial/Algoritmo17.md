# Exercício 17

[**Ver Análise**](Analise17.md)

```markdown
Algoritmo "Q17 - Sequencial"
Var
   m, maux, a, s, id: inteiro
Inicio
   escreva("Insira os 10 algarismos do seu número de matrícula: ")
   leia(m)
   escreval
   maux <- m
   a <- maux div 1000000
   maux <- maux - a * 1000000
   s <- maux div 100000
   id <- maux - s * 100000
   escreval("Matrícula:", m)
   escreval("Ano:", a)
   escreval("Semestre:", s)
   escreval("Identificação única:", id)
Fimalgoritmo
