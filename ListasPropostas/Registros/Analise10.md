# Exercício 10

[*Ver Algoritmo*](Algoritmo10.md)

 *A companhia aérea VoeBem tem aeroportos em diferentes cidades do país. Para melhor gerenciar as viagens, os aeroportos contém um código, o nome da cidade onde se situam, a quantidade de voos de embarque e a quantidade de voos de desembarque. Cada voo é identificado com o código do aeroporto de origem e do aeroporto de destino. A VoeBem informou que identifica seus aeroportos com um código inteiro único entre 0 e o número de aeroportos existentes.*

*Faça um pseudocódigo que controle o fluxo de 10 voos em 5 aeroportos.*

**Entrada**

- O código, nome da cidade, quantidade de voos que saem e que chegam de cada um dos 5 aeroportos e o código do aeroporto de origem e o código do aeroporto de destino de cada um dos 10 voos.

**Saída**

- A impressão dos dados dos 10 voos e dos aeroportos após o fim do dia.

**Restrições**

- o nome deve ser preenchido e conter até 15 caracteres.
- não devem ser aceitos nomes e códigos repetidos.
- o código de um aeroporto deve estar entre 0 e 4.
- a quantidade de voos que saem ou entram é sempre maior que 0.
- um voo só é realizado se existir algum aeroporto com vaga para embarque e outro aeroporto com vaga para desembarque.

**Exemplo**

| Entrada| Saída  |
|--------------------------|------------------------------------|
|//código, nome, voos que chegam, voos que saem<br>a1: 1, “Brasília”, 5, 2<br>a2: 0, “São Paulo”, 1, 10<br>a3: 2, “Rio de Janeiro”, 5, 7<br>//aeroporto de origem, aeroporto de destino<br>voo 1: 1, 2<br>voo 2: 0, 1<br>voo 3: 2, 0<br>voo 4: 1, 0<br>voo 5: 2, 1|AEROPORTO 1<br>Código 1.<br>Nome:Brasília.<br>Voos de entrada: 3.<br>Voos de saída: 0.<br>AEROPORTO 2<br>Código: 0.<br>Nome:São Paulo.<br>Voos de entrada: 0.<br>Voos de saída: 8.<br>AEROPORTO 3<br>Código: 2.<br>Nome:Rio de Janeiro.<br>Voos de entrada: 3.<br>Voos de saída: 6.<br>VOO 1<br>Entrada: Brasília. (CÓD 1).<br.Saída: Rio de Janeiro. (CÓD 2).<br>VOO 2<br>Entrada: São Paulo. (CÓD 0).<br>Saída: Brasília. (CÓD 1).<br>VOO 3<br>Entrada: Rio de Janeiro. (CÓD 2).<br>Saída: São Paulo. (CÓD 0).<br>VOO 4<br>Entrada: Brasília. (CÓD 1).<br>Saída: São Paulo. (CÓD 0).<br>VOO 5<br>Entrada: Rio de Janeiro. (CÓD 2).<br>Saída: Brasília. (CÓD 1).|
|a1: 1, “Belo Horizonte”, 2, 2<br>a2: 2, “Porto Alegre”, 1, 1<br>a3: 4, “Curitiba”, 1, 1<br>voo 1: 1, 4<br>voo 2: 0, 1<br>voo 3: 4, 0|Não é possível realizar mais voos porque não existem vagas de embarque ou desembarque entre os aeroportos.|<br>AEROPORTO 1<br>Código: 1.<br>Nome: Belo Horizonte.<br>Voos de entrada: 1.<br>Voos de saída: 1.<br>AEROPORTO 2<br>Código: 2.<br><Nome: Porto Alegre.<br>Voos de entrada: 0.<br>Voos de saída 0.<br>AEROPORTO 3<br>Código: 4.<br>Nome: Curitiba.<br>Voos de entrada: 0.<br>Voos de saída: 0.<br>VOO 1<br>Entrada: Belo Horizonte. (CÓD 1).<br>Saída: Porto Alegre. (CÓD 2).<br>VOO 2<br>Entrada: Curitiba. (CÓD 4).<br>Saída: Belo Horizonte. (CÓD 1).<br>VOO 3<br>Entrada: Porto Alegre. (CÓD 2).<br>Saída:Curitiba.(CÓD 4).|
|a1: 0, “Santa Catarina”, 10, 7 a2: 5|Erro: código inválido. Insira um número entre 0 e 4:|
|a1: 4, “Fortaleza”, 1, 0|Erro: valor inválido. Insira um número maior que 0:|
|a1: 1, “São Paulo”, 1, 20<br>a2: 2, “Manaus”, 10, 30<br>a3: 4, “Goiânia”, 1, 1<br>voo 1: 5|Erro: código inválido. Insira um número entre 0 e 4:|
|a1: 1, “Brasília”, 1, 20<br>a2: 3, “São Paulo”, 10,30<br>a3: 0, “Rio de Janeiro”, 12, 1<br>voo 1: 1, 3<br>voo 2: 1, 0|Erro: esse aeroporto não possui mais voos de embarque. Insira um outro:|
|a1: 1, “Belo Horizonte”, 22, 31<br>a2: 2, “Porto Alegre”, 1, 10<br>a3: 4, “Curitiba”, 12, 1<br>voo 1: 1, 4<br>voo 2: 2, 4|Erro: esse aeroporto não possui mais voos de desembarque. Insira um outro:|