# Exercício 04

[**Ver Análise**](Analise04.md)

```markdown
Algoritmo "Q4 - Registros"
Tipo CoordenadaPolar = Registro
  r: real
  a: real
fimRegistro

Tipo CoordenadaCartesiana = Registro
  x: real
  y: real
fimRegistro

Var
  pontoPolar: CoordenadaPolar
  pontoCartesiano: CoordenadaCartesiana

Inicio
  escreva("Insira o raio da coordenada polar: ")
  leia(pontoPolar.r)
  escreva("Insira o argumento: ")
  leia(pontoPolar.a)

  se (pontoPolar.a >= (2 * pi)) entao
    pontoPolar.a <- pontoPolar.a mod (2 * pi)
  fimse

  pontoCartesiano.x <- pontoPolar.r * cos(pontoPolar.a)
  pontoCartesiano.y <- pontoPolar.r * sen(pontoPolar.a)

  escreval
  escreval("COORDENADAS POLARES")
  escreval("Raio:", pontoPolar.r)
  escreval("Argumento:", pontoPolar.a)
  escreval
  escreval("COORDENADAS CARTESIANAS")
  escreval("x:", pontoCartesiano.x)
  escreval("y:", pontoCartesiano.y)

Fimalgoritmo
