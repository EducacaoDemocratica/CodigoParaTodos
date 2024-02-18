# Exercício 50

[*Ver Algoritmo*](Algoritmo50.md)

*Ainda no estacionamento, tem-se que cada carro quando deixa o local deve ter o seu espaço disponibilizado no aplicativo, logo se era 1 passa a ser 0. Aprimore o pseudocódigo permitindo a escolha de uma função para a chegada e para a saída de um carro do estacionamento, lembrando que um veículo só poderá deixar o estacionamento se houver algum espaço ocupado. Use uma variável para selecionar uma função.*

**Entrada**

- A função do sistema (preencher ou liberar vaga) e as vagas a serem preenchidas ou liberadas.  

**Saída**

- O preenchimento da vaga selecionada se estiver disponível ou a liberação de uma vaga se estiver ocupada.

**Restrições**

- as vagas vão de 1 a 30.
- uma vaga só pode ser ocupada se estiver livre.
- uma vaga só pode ser liberada se estiver ocupada.

**Exemplo**
*Nota: Utilizando dez números*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|//1º loop<br>f: preencher<br>vagas: 3, 7, 8, 10, 11, 13, 17,18, 28, 29.<br>//2º loop<br>f: liberar<br>vagas: 3, 10, 18, 28.<br>/3º loop <br>f: sair|//1º loop<br> Vagas preenchidas com sucesso.<br>//2º loop<br>Vagas liberadas com sucesso.<br>//3º loop<br>Sistema encerrado com sucesso.|
|f: liberar| Erro: não existem vagas ocupadas. Preencha uma vaga:|
|//1º loop<br>f: preencher<br>vagas: 3, 7, 8, 10, 11, 13, 17,18, 28, 29<br>//2º loop<br>f: liberar<br>vagas: 3, 10, 18, 28.<br>//3º loop<br>f: sair|//1º loop<br>Vagas preenchidas com sucesso.<br>//2º loop<br>Vagas liberadas com sucesso.<br>//3º loop<br> Sistema encerrado com sucesso.|
|f: liberar| Erro: não existem vagas ocupadas. Preencha uma vaga|
|//1º loop <br> f: preencher<br> vagas: 3,7,8,10,11,13,17,18,28,29<br>//2º loop<br>f: liberar<br> vaga 12.|//1º loop<br> Vagas preenchidas com sucesso.<br>//2º loop<br> Esta vaga não está preenchida|
|f: preencher<br>vagas: 1, 5, 8, 9, 10, 12, 16,17, 28, 31.| Erro: essa vaga não existe. Escolha outra:|