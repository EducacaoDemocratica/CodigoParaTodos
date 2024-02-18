# Exercício 51

[*Ver Algoritmo*](Algoritmo51.md)

*Por fim, para um melhor controle, foi necessário a utilização dos 4 números da placa do carro para indicar uma vaga ocupada para acrescentar a funcionalidade de localização do veículo, afinal, não é incomum que um cliente esqueça onde estacionou seu veículo. Aprimore o pseudocódigo para agregar essa funcionalidade e permitir a consulta do local de estacionamento do veículo. Suponha que as placas não iniciam no dígito 0. Não permita a entrada de placas duplicadas.*

**Entrada**

- A função do sistema (preencher, liberar ou procurar vaga) e as vagas a serem preenchidas ou liberadas.  

**Saída**

- O preenchimento da vaga selecionada se estiver disponível ou a liberação de uma vaga se estiver ocupada ou a localização do veículo.

**Restrições**

- as vagas vão de 1 a 30.
- uma vaga só pode ser ocupada se estiver livre.
- uma vaga só pode ser liberada se estiver ocupada.
- uma placa deve ter 4 dígitos não começando por 0.
- o estacionamento não deve ter placas duplicadas.

**Exemplo**
*Nota: Utilizando dez números*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|//1º loop<br>f: preencher<br>vagas: 3, 7 <br>placa: 2191; 3899.<br>//2º loop<br>f: liberar<br>vagas: 31.<br>/3º loop <br>f: procurar placa<br>placa: 9192.<br>//5º loop<br> f: procurar placa<br>placa: 0121<br>//6º loop<br>f: liberar<br>vaga: 3<br>//7º loop<br>f: liberar<br> vaga: 1<br>//8º loop<br>f: sair|//1º loop<br>Vagas preenchidas com sucesso.<br>//2º loop<br>Essa vaga não existe.<br>//3º loop<br>Esse veículo está estacionado na 3ª vaga<br>//4º loop<br>Veículo não encontrado.<br>//5º loop<br>Placa inválida.<br>//6º loop<br>Vaga liberada com sucesso.<br>//7º loop<br>Essa vaga não está ocupada.<br>//8º loop<br>Sistema encerrado com sucesso.|