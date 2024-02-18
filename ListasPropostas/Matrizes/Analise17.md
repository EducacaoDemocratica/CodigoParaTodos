# Exercício 17

[*Ver Algoritmo*](Algoritmo17.md)

 *Uma floricultura conhecedora de sua clientela gostaria de um sistema que
pudesse controlar sempre o estoque de determinadas plantas, pois todos os dias
o dono faz novas aquisições. Faça um pseudocódigo que cadastre 50 dados de
plantas, sendo eles o nome, o estoque ideal e a quantidade em estoque. Imprima
uma lista das plantas que estão com o estoque abaixo do ideal e a respectiva
quantidade que o dono da loja precisa comprar no próximo dia.*

**Entrada**

- O nome, quantidade em estoque e a quantidade ideal de cada uma das 50 plantas.

**Saída**

- A lista com as plantas com estoque abaixo do ideal e a quantidade a ser comprada
para repor o estoque de cada planta.

**Restrições**

- o dono da floricultura disse que não existem plantas com nomes repetidos.
- a quantidade ideal deve ser maior que 0.
- a quantidade em estoque não deve ser negativa.

**Exemplo**


| Entrada | Saída |
|-|-|
|//nome; estoque; estoque ideal<BR>planta 1: “Girassol”, 20, 15<BR>planta 2: “Suculenta”, 5, 8<BR>planta 3: “Cacto”, 10, 12<BR>planta 4: “Tulipa”, 15, 10<BR>planta 5: “Margarida”, 10, 8|Plantas abaixo do estoque e quantidade necessária para reposição:<BR>Suculenta: é necessário comprar mais 3 unidades.<BR>Cacto: é necessário comprar mais 2 unidades.|
|planta 1: “Orquídea”, 10, 10<BR>planta 2: “Jasmin”, 50, 40<br>planta 3: “Acácia”, 30, 30<BR>planta 4: “Bétula”, 10, 5<BR>
planta 5: “Bromélia”, 20, 18|Não existem plantas com quantidade abaixo do estoque.|
|lanta 1: “Lírio”, 10, 10<BR>planta 2: “Lírio”, 50, 40|Erro: esse nome já foi cadastrado. Insira outro:|
|planta 1: “Rosas do Campo”, - |Erro: a quantidade em estoque não
1, 10 deve ser negativa. Insira outro número:|
|planta 1: “Rosas Vermelhas”,| Erro: a quantidade ideal deve ser
10, 0 maior que 0. Insira outro número:|