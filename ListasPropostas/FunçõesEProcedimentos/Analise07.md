# Exercício 07

[**Ver Algoritmo**](Algortimo07.md)

*Filas são estruturas de dados do tipo FIFO (first-in, first-out) em que o primeiro
elemento a ser inserido será o primeiro a ser retirado, ou seja, adiciona-se itens no
fim e remove-se do início. Assim, uma fila permite acesso a apenas um de seus
elementos - o primeiro inserido. Para processar o segundo item inserido, você deve
remover o primeiro.*

*A implementação de uma fila pode ser realizada através de um vetor.
A manipulação dos elementos de uma fila é realizada em apenas uma das
extremidades do vetor, uma chamada de início, onde entram e saem os valores.
Em oposição ao início, na outra extremidade está o final, a última posição do
vetor.*
*Todas as operações em uma fila podem ser imaginadas como as que ocorrem
numa fila de pessoas num banco, exceto que os elementos se movem na fila
somente quando o primeiro elemento é retirado:*


*- enfileirar: colocar um elemento na fila;<BR>- desenfileirar: retirar um elemento na fila;<BR>- mostrar a fila: exibe todos os elementos da fila;<BR>- verificar se a fila está vazia;<BR>- verificar se a fila está cheia;*



*Faça um pseudocódigo que simule uma fila de até 20 elementos, sem repetição
entre eles, com todas as suas operações utilizando módulos e passagem de
parâmetros.
NÃO É PERMITIDO USAR VARIÁVEIS GLOBAIS, exceto variáveis compostas como vetores,
matrizes e registros.
Você pode criar filas do que quiser, seja de tipos primitivos ou até mesmo de novos tipos.*


**Entrada**

- enfileirar: um elemento da fila;
- desenfileirar, mostrar o topo, verificar se está vazia, verificar se está
cheia: nenhuma.


**Saída**

- O resultado de cada módulo realizado.
  
**Restrições**

- não adicione elementos repetidos à pilha;
- não utilize variáveis globais.

**Exemplo**
| Entrada | Saída | 
|-|-|
|mostrar a fila()<BR><BR>enfileirar()<BR>“ ”<BR><BR>verificar se está vazia():<BR><BR>enfileirar()<BR>“Luiza”<BR><BR>enfileirar()<BR>“Gabriel”<BR>enfileirar()<BR>“Mateus”<BR><BR>enfileirar()<BR>“Tiago”<BR>enfileirar()<BR>“Maurílio”<BR>enfileirar()<BR><BR>mostrar a fila()<BR>desenfileirar()<BR><BR>verificar se está cheia()<BR><BR>mostrar a fila()|mostrar a fila():A fila está vazia. Adicione um elemento!<BR><BR>enfileirar():Insira um elemento válido à fila:<BR><BR>verificar se está vazia():A fila está vazia.<BR><BR>enfileirar(): Elemento inserido com sucesso!<BR><BR>enfileirar():Elemento inserido com sucesso!<BR><BR>enfileirar():Elemento inserido com sucesso!<BR><BR>enfileirar():Elemento inserido com sucesso!<BR><BR>enfileirar():Elemento inserido com sucesso!<BR><BR>enfileirar():Elemento inserido com sucesso!<BR><BR>mostrar a fila():1º elemento: LUIZA<BR>2º elemento: GABRIEL<BR>3º elemento: MATEUS<BR>4º elemento: TIAGO<BR>5º elemento: MAURÍLIO<BR><BR>desenfileirar():Elemento LUIZA removido com sucesso.<BR><BR>verificar se está cheia():A fila está cheia.<BR><BR>mostrar a fila():1º elemento: GABRIEL<BR>2º elemento: MATEUS<BR>3º elemento: TIAGO<BR>4º elemento: MAURÍLIO<BR>
