# Exercício 08

[**Ver Algoritmo**](Algortimo08.md)

*Pilhas são estruturas de dados do tipo LIFO (last-in, first-out) em que o
último elemento a ser inserido será o primeiro a ser retirado. Assim, uma pilha
permite acesso a apenas um de seus elementos - o último inserido. Para
processar o penúltimo item inserido, deve-se remover o último.
A implementação de uma pilha pode ser realizada através de um vetor.
A manipulação dos elementos de uma pilha é realizada em apenas uma das
extremidades do vetor, uma chamada de topo, onde entram e saem os valores.
Em oposição ao topo, na outra extremidade está a base, é a última posição do
vetor (o primeiro valor que entrou).
Todas as operações em uma pilha podem ser imaginadas como as que ocorre
numa pilha de pratos em um restaurante ou como num jogo com as cartas de
um baralho:*


*- empilhar/push: colocar um elemento na pilha;<BR>- desempilhar/pop: retirar um elemento da pilha;<BR>- mostrar o topo: exibir o elemento no início da pilha;<BR>- verificar se a pilha está vazia;<BR>- verificar se a pilha está cheia;*



*Faça um pseudocódigo que simule uma pilha de até 20 elementos, sem repetição
entre eles, com todas as suas operações utilizando módulos e passagem de
parâmetros.
NÃO É PERMITIDO USAR VARIÁVEIS GLOBAIS, exceto variáveis compostas como vetores,
matrizes e registros.
Você pode criar filas do que quiser, seja de tipos primitivos ou até mesmo de novos tipos.*


**Entrada**

- push: um elemento da fila;
- pop, mostrar o topo, verificar se está vazia, verificar se está cheia:
nenhuma.


**Saída**

- O resultado de cada módulo realizado.
  
**Restrições**

- não adicione elementos repetidos à pilha;
- não utilize variáveis globais.

**Exemplo**
<sub>Nota: usando uma pilha de nomes de até 5 elementos;
| Entrada | Saída | 
|-|-|
| mostrar o topo()<BR><BR>verificar se está vazia()<BR><BR>push()<BR>“Maria”<BR><BR>verificar se está vazia()<BR><BR>push()<BR>“Maria”<BR><BR>push()<BR>“João”<BR><BR>push()<BR>“Ana”<BR><BR>push()<BR>“José”<BR><BR>push()<BR>“Cauê”<BR><BR>push()<BR><BR>verificar se está cheia()<BR><BR>pop()<BR><BR>verificar se está cheia()<BR><BR>mostrar o topo()|mostrar o topo(): A pilha está vazia. Adicione um elemento!<BR><BR>verificar se está vazia():A pilha está vazia.<BR><BR>push():Elemento inserido com sucesso!<BR><BR>verificar se está vazia():A pilha não está vazia<BR><BR>push():Esse elemento já está inserido!<BR><BR>push():Elemento inserido com sucesso!<BR><BR>push():Elemento inserido com sucesso!<BR><BR>push():Elemento inserido com sucesso!<BR><BR>push():Elemento inserido com sucesso!<BR><BR>push():A pilha está cheia. Remova um elemento!<BR><BR>verificar se está cheia():A pilha está cheia<BR><BR>pop():Elemento CAUÊ removido com sucesso.<BR><BR>verificar se está cheia():A pilha não está cheia<BR><BR>mostrar o topo():Topo da fila: 4 elemento - JOSÉ|
