# Exercício 07
[**Ver Análise**](Analise07.md)
```
Algoritmo "Q7 - exSequencial"

Var

  n: inteiro
  
  r1, r2: real

Inicio

  escreval("A expressão 'n² + 2.n + 1' tem mesmo valor que '(n+1)²'?")
  
  escreval
  
  escreva("Insira um número inteiro: ")
  
  leia(n)
  
  r1 <- (n^2) + (2 * n) + 1
  
  r2 <- (n+1)^ 2
  
  escreval("Os resultados foram: ")
  
  escreval
  
  escreval(n,"² + 2 *", n," + 1 ->", n ^ 2," +", 2 * n," + 1 =", r1)
  
  escreval("(", n," + 1 )² -> (", n + 1," )² = ", r2)

Fimalgoritmo
