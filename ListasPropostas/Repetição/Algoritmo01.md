# Exercício 40

[**Ver Análise**](Analise40.md)

```markdown
Algoritmo "Q40 - Condicional"
Var
   k, kfinal, b, imp, vcl, vc, vtaxa, vtotal: real
   c, cl, n: inteiro
Inicio
   escreva("Insira o valor do kWh: ")
   leia(k)

   se (k <= 0) entao
      escreval("Valor negativo ou nulo encontrado.")
   senao
      escreva("Quantos kWh foram consumidos? ")
      leia(c)

      se (c < 0) entao
         escreval("Valor negativo encontrado.")
      senao
         escreva("Qual o custo da bandeira vigente? R$")
         leia(b)

         se (b <= 0) entao
            escreval("Valor negativo ou nulo encontrado.")
         senao
            escreva("Qual a taxa fixa de iluminação pública? R$")
            leia(vtaxa)

            se (vtaxa <= 0) entao
               escreval("Valor negativo ou nulo encontrado.")
            senao
               escreval("Insira sua classe: ")
               escreval("1 - Monofásica | 2 - Bifásica | 3 - Trifásica")
               leia(cl)

               se ((cl < 1) ou (cl > 3)) entao
                  escreval("O valor inserido não é válido.")
               senao
                  se (cl = 1) entao
                     cl <- 30
                  senao
                     se (cl = 2) entao
                        cl <- 50
                     senao
                        cl <- 100
                     fimse
                  fimse

                  escreval("Insira a natureza de seu estabelecimento:")
                  escreval("1 – Normal")
                  escreval("2 – Rural")
                  escreval("3 – Industrial")
                  escreval("4 – Baixa renda")
                  leia(n)

                  se ((n < 1) ou (n > 4)) entao
                     escreval("O valor inserido não é válido.")
                  senao
                     se (n = 1) entao
                        kfinal <- k
                     senao
                        se (n = 2) entao
                           kfinal <- k * 0.7
                        senao
                           se (n = 3) entao
                              kfinal <- k * 1.25
                           senao
                              kfinal <- k * 0.35
                           fimse
                        fimse
                     fimse
                  fimse
               fimse

               vc <- kfinal * c
               vcl <- k * cl
               imp <- vc * 0.34
               vtotal <- vc + vcl + vtaxa + imp

               escreval
               escreval("kWh base: R$", k)
               escreval("kWh da natureza: R$", kfinal)
               escreval("Valor de consumo: R$", vc)
               escreval("Valor de classe: R$", vcl)
               escreval("Iluminação pública: R$", vtaxa)
               escreval("Imposto: R$", imp)
               escreval("Valor total: R$", vtotal)
            fimse
         fimse
      fimse
   fimse
Fimalgoritmo
