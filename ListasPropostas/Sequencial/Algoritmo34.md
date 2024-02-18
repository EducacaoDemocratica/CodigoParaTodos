# Exercício 34

[**Ver Análise**](Analise34.md)

```markdown
Algoritmo "Q34 - Sequencial"
Var
   c, i, j, vt: real
   t: inteiro
Inicio
   escreva("Insira o valor do capital empregado: R$")
   leia(c)
   escreva("Insira o valor da taxa de juros cobrada(%): ")
   leia(i)
   escreva("Insira o tempo de duração da transação(meses): ")
   leia(t)
   escreval
   j <- (c * i * t)/100
   vt <- c + j
   escreval("Valor real da transação : R$", c:6:2, ".")
   escreval("Taxa de juros aplicada:", i:6:2, "%.")
   escreval("Tempo de transação:", t, " meses.")
   escreval("Total de juros cobrado: R$", j:6:2, ".")
   escreval("Valor total a ser pago: R$", vt:6:2, ".")
Fimalgoritmo
