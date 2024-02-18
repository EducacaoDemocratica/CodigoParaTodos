# Exercício 27

[**Ver Análise**](Analise27.md)

```markdown
Algoritmo "Q27 - Condicional"
Var
   r, d, aux, cr, cd, cdbr, vr, vd, vdbr, casac, casabr: real
Inicio
   escreval("Cotação atual das moedas no Brasil")
   escreval
   escreva("Insira a cotação do dólar (US$1,00): ")
   leia(cdbr)

   se (cdbr <= 0) entao
      escreval("Erro: valor inválido encontrado.")
   senao
      escreval
      escreval("Cotação atual das moedas no Chile")
      escreval
      escreva("Insira a cotação do real (R$1,00): ")
      leia(cr)

      se (cr <= 0) entao
         escreval("Erro: valor inválido encontrado.")
      senao
         escreva("Insira a cotação do dólar (US$1,00): ")
         leia(cd)

         se (cd <= 0) entao
            escreval("Erro: valor inválido encontrado.")
         senao
            escreval
            escreval("Quantidade de moedas do usuário")
            escreval
            escreva("Insira a quantidade de real que você carrega: R$")
            leia(r)

            se (r < 0) entao
               escreval("Erro, valor inválido encontrado.")
            senao
               escreva("Insira a quantidade de dólar que você carrega: US$")
               leia(d)

               se (d < 0) entao
                  escreval("Erro, valor inválido encontrado.")
               senao
                  vr <- r * cr
                  vd <- d * cd
                  aux <- d * cdbr
                  vdbr <- aux * cr
                  casac <- vr + vd
                  casabr <- vr + vdbr

                  escreval

                  se (vd = vdbr) entao
                     escreval("A troca pode ser realizada tanto na casa brasileira como na chilena.")
                  senao
                     se (vd > vdbr) entao
                        escreval("É mais vantajoso realizar as trocas em uma casa chilena.")
                     senao
                        escreval("É mais vantajoso trocar o dólar em uma casa brasileira e depois trocar os reais na casa chilena.")
                     fimse
                  fimse

                  escreval
                  escreval("Valor trocado somente na casa chilena: ", casac,".")
                  escreval("Valor trocado na casa brasileira e chilena: ", casabr,".")
               fimse
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
