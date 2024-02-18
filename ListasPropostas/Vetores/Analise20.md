# Exercício 20

[*Ver Algoritmo*](Algoritmo20.md)

*A busca de um valor pode ser otimizada em um vetor ordenado, pois se o valor que estiver na posição do vetor no momento da comparação for maior que o valor procurado, você já pode dar por encerrada a busca, uma vez que o valor não se encontra na estrutura, evitando assim, perder tempo com comparações desnecessárias.* Faça um pseudocódigo que armazene 80 números inteiros em um vetor e indique se um número `n` inteiro qualquer informado pelo usuário está presente no vetor.

**Entrada**
- 80 números inteiros e um número inteiro `n`.

**Saída**
- Se `n` está presente no vetor.

**Restrições**
- Faça a busca de maneira otimizada (ordene e comece a buscar. Caso a posição do vetor naquele instante for maior que `n`, encerre a procura).

**Exemplo**
Nota: utilizando 10 números.

| Entrada                                       | Saída                            |
| --------------------------------------------- | -------------------------------- |
| Números: 7, 0, 9, 10, 5, 5, 7, 2, 5, 4   <br>n: 4      |   Está presente na estrutura. |
| Números: 5, 2, 7, 0, 1, 4, 0, 3, 4, 5   <br> n: 9         |Não está presente na estrutura. |
| Números: 1, 8, 4, 8, 10, -3, -5, 6, 7, -9   <br>n: -5   |   Está presente na estrutura. |
