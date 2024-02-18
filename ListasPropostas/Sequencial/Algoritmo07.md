# Exercício 07

[**Ver Análise**](Analise07.md)

```markdown
Algoritmo "Q7 - Sequencial"
Var
   p1, p2, r, a, p: real
Inicio
   escreva("Insira a medida em metros da parede no comprimento da sala:")
   leia(p1)
   escreva("Insira a medida em metros da parede na largura da sala: ")
   leia(p2)
   screval
   r <- p1 * 2 + p2 * 2
   a <- p1 * p2
   p <- a / (0.6^2)
   escreval("Comprimento da sala:", p1, "m.")
   escreval("Largura da sala:", p2, "m.")
   escreval("Perímetro/quantidade de rodapé necessário:", r, "m.")
   escreval("Área da sala:", a, "m².")
   escreval("Quantidade de pisos:", p, "unidades.")
Fimalgoritmo
