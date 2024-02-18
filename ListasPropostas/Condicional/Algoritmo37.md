# Exercício 37

[**Ver Análise**](Analise37.md)

```markdown
Algoritmo "Q37 - Condicional"
Var
   data, dia, mes, ano: inteiro
Inicio
   escreva("Insira a data no formato DDMMAAAA: ")
   leia(data)

   se (data < 0) entao
      escreval("Erro: a data inserida é negativa.")
   senao
      dia <- data div 1000000
      data <- data - (dia * 1000000)
      mes <- data div 10000
      ano <- data - (mes * 10000)

      se (dia = 0) entao
         escreval("Erro: não há dia 0.")
      senao
         se (mes = 0) ou (mes > 12) entao
            escreval("O mês", mes," não existe.")
         senao
            se (ano = 0) ou (ano > 9999) entao
               escreval("O ano", ano, " não se encaixa no padrão AAAA.")
            senao
               se ((mes = 2) e (dia > 28)) entao
                  escreval("Fevereiro tem apenas 28 dias.")
               senao
                  se ((((mes < 7) e (mes mod 2 = 0)) ou ((mes > 8) e (mes mod 2 = 1))) e (dia > 30)) entao
                     escreval("No mês inserido, há apenas 30 dias.")
                  senao
                     se (dia > 31) entao
                        escreval("Não há mais de 30 dias por mês.")
                     senao
                        se ((ano > 2000) e (ano < 2101)) entao
                           escreval("A data é válida para o século XXI.")
                        senao
                           escreval("A data não é válida ao século XXI.")
                        fimse
                     fimse
                  fimse
               fimse
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
