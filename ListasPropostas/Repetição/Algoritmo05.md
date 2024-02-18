# Exercício 05

[**Ver Análise**](Analise05.md)

```markdown
Algoritmo "Q5 - Repeticao"
Var
   lsup, i, nescolhido, qmeninas, qmeninos, maior: inteiro
   nome, sexo, nomemaior: caractere
Inicio
   lsup <- 40
   maior <- 0
   para i de 1 ate lsup faca
      escreva("Escreva o nome: ")
      leia(nome)
      enquanto (nome = "") faca
         escreva("Não preencha com espaços vazios: ")
         leia(nome)
      fimenquanto
      escreva("Insira o sexo do aluno (F - Feminino; M - Masculino): ")
      leia(sexo)
      sexo <- maiusc(sexo)
      enquanto ((sexo = "") ou ((sexo <> "F") e (sexo <> "M"))) faca
         escreva("Não preencha com espaços vazios ou diferentes de 'F'/'M': ")
         leia(sexo)
         sexo <- maiusc(sexo)
      fimenquanto
      escreva("Escreva o número escolhido: ")
      leia(nescolhido)
      enquanto (nescolhido <= 0) faca
         escreva("O número deve ser maior que 0: ")
         leia(nescolhido)
      fimenquanto
      se (nescolhido > maior) entao
         maior <- nescolhido
         nomemaior <- nome
      fimse
      se (sexo = "F") entao
         se (nescolhido mod 5 = 0) entao
            qmeninas <- qmeninas + 1
         fimse
      senao
         se (nescolhido mod 2 = 0) entao
            qmeninos <- qmeninos + 1
         fimse
      fimse
   fimpara
   escreval
   escreval("Primeira pessoa que escolheu o maior número:", nomemaior)
   escreval("Quantidade de meninos que escolheram números pares:", qmeninos)
   escreval("Quantidade de meninas que escolheram algum número divisível por 5:", qmeninas)
Fimalgoritmo
