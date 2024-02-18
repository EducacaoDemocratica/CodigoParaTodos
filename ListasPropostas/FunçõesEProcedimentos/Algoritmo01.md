# Exercício 01

[**Ver Análise**](Analise01.md)

```markdown
Algoritmo "Q1 - FuncaoProcedimento"

procedimento preencheMatriz()
Var
  n, i, j: inteiro
Inicio
  para i de 1 ate lsupl faca
    para j de 1 ate lsupc faca
      n <- j + ((i - 1) * lsupc)
      escreva("Insira o ", n, "º valor da matriz: ")
      leia(m[i, j])
      v[n] <- m[i, j]
    fimpara
  fimpara
fimProcedimento

procedimento ordenaMatriz()
Var
  i, j, aux, n: inteiro
Inicio
  para j de ((lsupl * lsupc) - 1) ate 1 passo -1 faca
    para i de 1 ate j faca
      se (v[i] > v[i + 1]) entao
        aux <- v[i]
        v[i] <- v[i + 1]
        v[i + 1] <- aux
      fimse
    fimpara
  fimpara

  para i de 1 ate lsupl faca
    para j de 1 ate lsupc faca
      n <- j + ((i - 1) * lsupc)
      m[i, j] <- v[n]
    fimpara
  fimpara
fimProcedimento

procedimento imprimeMatriz()
Var
  i, j: inteiro
Inicio
  para i de 1 ate lsupl faca
    para j de 1 ate lsupc faca
      escreva(m[i, j], ", ")
    fimpara
    escreval
  fimpara
fimProcedimento

funcao leNumero(): inteiro
Var
  n: inteiro
Inicio
  leia(n)
  enquanto ((n <= 0) ou (n > 20)) faca
    escreva("Insira valores de 1 a 20: ")
    leia(n)
  fimenquanto
  retorne n
fimFuncao

Var
  m: vetor [1..20, 1..20] de inteiro
  v: vetor [1..400] de inteiro
  lsupl, lsupc: inteiro

Inicio
  escreva("Insira o número de linhas: ")
  lsupl <- leNumero()
  escreva("Insira o número de colunas: ")
  lsupc <- leNumero()
  preencheMatriz()
  escreval
  escreval("Matriz antes da ordenação: ")
  escreval
  imprimeMatriz()
  ordenaMatriz()
  escreval
  escreval("Matriz depois da ordenação: ")
  escreval
  imprimeMatriz()

Fimalgoritmo
