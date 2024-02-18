# Exercício 04

[**Ver Algoritmo**](Algortimo04.md)

*A caderneta de poupança é um serviço oferecido pelos bancos onde qualquer
cidadão pode abrir uma conta nesta modalidade e guardar seu dinheiro para uso
futuro. Ao abrir uma conta, o cidadão deve informar sua idade, pois não é permitido
que menores de 18 anos possuam contas em bancos. Outros dados são solicitados
como nome, CPF e telefone que devem ser válidos. A partir de então, um número é
gerado para identificar a conta de caderneta de poupança aberta e o cidadão já
consegue:*

*- depositar algum dinheiro;*

*- pedir um extrato que mostre o valor total depositado;*

*- retirar algum dinheiro (desde que o saldo seja suficiente para atender ao
pedido).*

*Faça um pseudocódigo que permita gerenciar ATÉ 30 contas bancárias, criando uma
conta, listando as contas, realizando depósitos, saques ou gerando o extrato de uma
conta.*


**Entrada**<sub>De acordo com cada módulo

- criar conta: idade, nome, CPF, telefone e endereço;
- depositar: o identificador da conta e o valor que deseja ser depositado;
- sacar: o identificador da conta e o valor que deseja ser retirado;
- gerar extrato: o identificador da conta;
- listar: nenhuma;

**Saída**

- O resultado de cada módulo realizado.
  
**Restrições**

- a idade mínima para criar uma conta é a de 18 anos;
- o CPF deve ser válido;
- o nome, telefone e endereço devem ser preenchidos corretamente;
- o sistema não aceita a entrada de CPFs e números de telefone duplicados;
- o saque, depósito e extrato só devem ser aceitos com identificadores válidos;
- o valor a ser depositado ou retirado deve ser maior que 0;
- um saque só é feito se o saldo da conta for maior ou igual ao valor que deseja ser retirado;

**Exemplo**

| Entrada | Saída | 
|-|-|
| listar()<BR><BR>criarConta():<br>idade: 20<BR>nome: “Maria”<BR>CPF: 422.782.070-75<BR>telefone: 31 99192-0111<<BR><BR>criarConta()<BR>idade: 17<BR>nome: “ ”<BR>CPF: 999.999.999.99<BR>telefone: 31 98117-02depositar()<BR>código: 1<BR>valor: 500<BR><BR>gerarExtrato()<BR>código: 1<BR><BR>sacar()<BR>código: 1<BR>valor:89.10<BR><BR>depositar()<BR>código: 2<BR>valor: 0|listar(): Não existem contas cadastradas.<BR>criarConta():CONTA CRIADA COM SUCESSO:<BR><BR>Código: 1.<BR>Cliente: Maria - 42278207075<BR>Saldo: R$ 0.00.<BR><BR>criarConta():<BR><BR>Idade inválida.<BR>Nome inválido.<BR>CPF inválido.<BR>Telefone inválido.<BR><BR>depositar(): DEPÓSITO REALIZADO COM SUCESSO<BR>Código: 1.<BR>Cliente: Maria - 42278207075<BR><BR>Antes do depósito:<BR>Saldo: R$ 0.00.<BR><BR>Após o depósito:<BR>Saldo: R$500.00.<BR><BR>gerarExtrato()<BR><BR>Código: 1.<BR>Cliente: Maria - 42278207075<BR>Saldo: R$500.00.<BR><BR>sacar(): SAQUE REALIZADO COM SUCESSO:<BR><BR>Código: 1.<BR>Cliente: Maria - 42278207075<BR><BR>Antes do saque:<BR>Saldo: R$500.00.<BR><BR>Após o saque:<BR>Saldo: R$410.90.<BR><BR>depositar(): Erro!<BR><BR>Código não encontrado.<BR> Valor inválido.|