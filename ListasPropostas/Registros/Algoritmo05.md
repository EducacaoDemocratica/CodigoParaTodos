# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - Registros"
Tipo numeroComplexo = Registro
  a: real
  b: real
  m: real
fimRegistro

Var
  z, w, s, d, p: numeroComplexo
  sinal: caractere

Inicio
  escreva("Insira a parte real de z: ")
  leia(z.a)
  escreva("Insira a parte imaginária de z: ")
  leia(z.b)

  enquanto (z.b = 0) faca
    escreva("A parte imaginária deve ser diferente de 0: ")
    leia(z.b)
  fimenquanto

  escreval
  escreva("Insira a parte real de w: ")
  leia(w.a)
  escreva("Insira a parte imaginária de w: ")
  leia(w.b)

  enquanto (w.b = 0) faca
    escreva("A parte imaginária deve ser diferente de 0: ")
    leia(w.b)
  fimenquanto

  z.m <- ((z.a ^ 2) + (z.b ^ 2))^(1/2)
  w.m <- ((w.a ^ 2) + (w.b ^ 2))^(1/2)

  s.a <- z.a + w.a
  s.b <- z.b + w.b

  d.a <- z.a - w.a
  d.b <- z.b - w.b

  p.a <- (z.a * w.a) - (z.b * w.b)
  p.b <- (z.a * w.b) + (z.b * w.a)

  escreval

  se (z.b < 0) entao
    sinal <- ""
  senao
    sinal <- " +"
  fimse

  escreval("z:", z.a, sinal, z.b,"i.")
  escreval("módulo de z:", z.m)

  se (w.b < 0) entao
    sinal <- ""
  senao
    sinal <- " +"
  fimse

  escreval
  escreval("w:", w.a, sinal, w.b,"i.")
  escreval("módulo de w:", w.m)

  se (s.b < 0) entao
    sinal <- ""
  senao
    sinal <- " +"
  fimse

  escreval
  escreval("Soma entre z e w:", s.a, sinal, s.b,"i.")

  se (d.b < 0) entao
    sinal <- ""
  senao
    sinal <- " +"
  fimse

  escreval("Diferença entre z e w:", d.a, sinal, d.b,"i.")

  se (p.b < 0) entao
    sinal <- ""
  senao
    sinal <- " +"
  fimse

  escreval("Produto entre z e w:", p.a, sinal, p.b,"i.")

Fimalgoritmo
