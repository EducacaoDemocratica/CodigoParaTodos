# Exercício 09

[**Ver Análise**](Analise09.md)

```markdown
Algoritmo "Q9 - Registros"
Const
  ERRO1 = "ERRO: PRODUTO NÃO ENCONTRADO!"
  ERRO2 = "ERRO: NÃO HÁ ESSA QUANTIA EM ESTOQUE!"
  SUCESSO = "PEDIDO REALIZADO COM SUCESSO!"

Tipo TProduto = registro
  codigo: inteiro
  nome: caractere
  preco: real
  estoque: inteiro
fimRegistro

Tipo TPedido = registro
  codigoProduto: inteiro
  quantidade: inteiro
  valor: real
  status: caractere
fimRegistro

Var
  produtos: vetor [1..5] de TProduto
  pedidos: vetor [1..3] de TPedido
  nomes: vetor [1..5] de caractere
  i, j, lsupProdutos, lsupPedidos, tam, aux: inteiro
  paux, caract: caractere

Inicio
  lsupProdutos <- 5
  lsupPedidos <- 3

  para i de 1 ate lsupProdutos faca
    escreva("Insira o código do", i,"º produto: ")
    leia(produtos[i].codigo)

    enquanto (produtos[i].codigo <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(produtos[i].codigo)
    fimenquanto

    j <- 1

    enquanto (j < lsupProdutos) faca
      se (j <> i) entao
        enquanto (produtos[i].codigo = produtos[j].codigo) faca
          escreva("Esse código já está cadastrado: ")
          leia (produtos[i].codigo)

          enquanto (produtos[i].codigo <= 0) faca
            escreva("Insira um valor maior que 0: ")
            leia(produtos[i].codigo)
          fimenquanto
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto

    j <- 1
    escreva("Insira o nome do", i,"º produto: ")
    leia(produtos[i].nome)
    paux <- ""
    tam <- compr(produtos[i].nome)

    para j de 1 ate tam faca
      caract <- copia(produtos[i].nome; j; 1)
      se (caract <> " ") entao
        paux <- paux + caract
    fimpara

    enquanto (paux = "") faca
      escreva("Não preencha com espaços vazios: ")
      leia(produtos[i].nome)
      paux <- ""
      tam <- compr(produtos[i].nome)

      para j de 1 ate tam faca
        caract <- copia(produtos[i].nome; j; 1)
        se (caract <> " ") entao
          paux <- paux + caract
      fimpara
    fimenquanto

    nomes[i] <- maiusc(paux)
    j <- 1

    enquanto (j < lsupProdutos) faca
      se (j <> i) entao
        enquanto (nomes[i] = nomes[j]) faca
          escreva("Esse nome já está cadastrado: ")
          leia (produtos[i].nome)
          paux <- ""
          tam <- compr(produtos[i].nome)

          para j de 1 ate tam faca
            caract <- copia(produtos[i].nome; j; 1)
            se (caract <> " ") entao
              paux <- paux + caract
          fimpara

          enquanto (paux = "") faca
            escreva("Não preencha com espaços vazios: ")
            leia(produtos[i].nome)
            paux <- ""
            tam <- compr(produtos[i].nome)

            para j de 1 ate tam faca
              caract <- copia(produtos[i].nome; j; 1)
              se (caract <> " ") entao
                paux <- paux + caract
            fimpara
          fimenquanto

          nomes[i] <- maiusc(paux)
        fimenquanto
      fimse

      j <- j + 1
    fimenquanto

    j <- 1
    escreva("Insira o preço: ")
    leia(produtos[i].preco)

    enquanto (produtos[i].preco <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(produtos[i].preco)
    fimenquanto

    escreva("Insira o estoque: ")
    leia(produtos[i].estoque)

    enquanto (produtos[i].estoque <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(produtos[i].estoque)
    fimenquanto

    escreval
  fimenquanto

  para i de 1 ate lsupPedidos faca
    aux <- 0
    escreva("Insira o código do produto do", i,"º pedido: ")
    leia(pedidos[i].codigoProduto)

    enquanto (pedidos[i].codigoProduto <= 0) faca
      escreva("Insira um valor maior que 0: ")
      leia(pedidos[i].codigoProduto)
    fimenquanto

    para j de 1 ate lsupProdutos faca
      se (pedidos[i].codigoProduto = produtos[j].codigo) entao
        aux <- j
      fimse
    fimpara

    se (aux <> 0) entao
      escreva("Insira a quantidade: ")
      leia(pedidos[i].quantidade)

      enquanto (pedidos[i].quantidade <= 0) faca
        escreva("Insira um valor maior que 0: ")
        leia(pedidos[i].quantidade)
      fimenquanto

      se (produtos[aux].estoque >= pedidos[i].quantidade) entao
        produtos[aux].estoque <- produtos[aux].estoque - pedidos[i].quantidade
        pedidos[i].status <- SUCESSO
        pedidos[i].valor <- produtos[aux].preco * pedidos[i].quantidade
      senao
        pedidos[i].status <- ERRO2
      fimse
    senao
      pedidos[i].status <- ERRO1
    fimse

    se (pedidos[i].status <> SUCESSO) entao
      escreval("Comportamento inesperado")
      (* Se chegar aqui, algo deu errado, e uma mensagem de erro foi impressa *)
    fimse

    escreval("Pedido encerrado!")
    escreval
  fimenquanto

  para i de 1 ate lsupProdutos faca
    escreval("PRODUTO", i)
    escreval("Código: ", produtos[i].codigo,".")
    escreval("Nome:", produtos[i].nome,".")
    escreval("Preço: R$", produtos[i].preco,".")
    escreval("Estoque: ", produtos[i].estoque,".")
    escreval
  fimenquanto

  para i de 1 ate lsupPedidos faca
    paux <- "DESCONHECIDO"
    para j de 1 ate lsupProdutos faca
      se (pedidos[i].codigoProduto = produtos[j].codigo) entao
        paux <- produtos[j].nome
      fimse
    fimpara

    escreval("PEDIDO", i)
    escreval("Produto: ", paux," (CÓDIGO: ", pedidos[i].codigoProduto,").")
    escreval("Quantidade:", pedidos[i].quantidade,".")
    escreval("Status: ", pedidos[i].status)
    escreval("Valor: R$", pedidos[i].valor,".")
    escreval
  fimenquanto

Fimalgoritmo
