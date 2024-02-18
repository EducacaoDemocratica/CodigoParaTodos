# Exercício 49

[*Ver Algoritmo*](Algoritmo49.md)

*Um supermercado está pensando em fazer um aplicativo para controlar as 30 vagas de estacionamento em seu pátio. Para fazer uma simulação do sistema, foi solicitado a criação de um pseudocódigo que controle esse espaço em que os espaços livres serão marcados com o número 0 e os espaços ocupados com o número 1. Faça um pseudocódigo que simule essa a entrada dos automóveis no estacionamento, lembrando que um veículo só poderá estacionar se houver um espaço vazio. Você pode implementar uma função para sair do sistema se achar necessário.*

**Entrada**

- As vagas que querem ser preenchidas.

**Saída**

- O preenchimento da vaga selecionada se essa estiver disponível.

**Restrições**

- as vagas vão de 1 a 30.
- uma vaga só pode ser ocupada se estiver livre.

**Exemplo**
*Nota: Utilizando dez números*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|1, 14, 12, 29, 10, 21, 30, 2, 9, 15|.Vagas preenchidas com sucesso.|
|9, 10, 30, 21, 18, 8, 6, 11, 2, 11.|Erro: essa vaga já está ocupada. Escolha outra:|
|12, 5, 8, 1, 4, 11, 32, 18, 22, 27.|Erro: essa vaga não existe. Escolha outra:|