# Exercício 31

[**Ver Análise**](Analise31.md)

```markdown
Algoritmo "Q31 - Condicional"
Var
   mes, placa, d: inteiro
Inicio
   escreva("Insira o mês atual: ")
   leia(mes)

   se ((mes <= 0) ou (mes > 12)) entao
      escreval("Erro: o mês inserido não existe.")
   senao
      escreva("Insira os 4 dígitos da placa do veículo: ")
      leia(placa)
      escreval

      se ((placa <= 0) ou (placa > 9999)) entao
         escreval("Erro: formato inválido encontrado.")
      senao
         placa <- placa - ((placa div 1000) * 1000)
         placa <- placa - ((placa div 100) * 100)
         d <- placa - ((placa div 10) * 10)
         escreval("Dígito verificador: ", d)

         se (d = 0) entao
            d <- 10
         fimse

         se (mes = d) entao
            escreval("O IPVA vence nesse mês.")
         senao
            se (mes > d) entao
               escreval("O IPVA venceu há ", mes - d, " mês/meses.")
            senao
               escreval("O IPVA vence daqui a ", d - mes, " mês/meses.")
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
