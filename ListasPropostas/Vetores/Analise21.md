# Exercício 21

[*Ver Algoritmo*](Algoritmo21.md)

*Faça um pseudocódigo que:*
*a. armazene 30 números inteiros em uma variável composta A;*<br>
*b. armazene 30 números inteiros em outra variável composta B;*<br>
*c. ordene A e B em ordem crescente;*<br>
*d. leia uma variável inteira x verifique qual elemento de A é igual a x através de uma procura otimizada;*<br>
*e. imprima os dois vetores e o elemento em B de posição correspondente ao elemento de A que é igual a x caso exista.*

**Entrada**
- *60 números inteiros e um número inteiro x.*

**Saída**
- *A impressão de A e B e do elemento no vetor B na mesma posição em que x está no vetor A caso exista.*

**Restrições**
- *Faça a procura de maneira otimizada.*

**Exemplo**
*Nota: utilizando 10 números.*

| Entrada                                       | Saída                                                |
| --------------------------------------------- | ---------------------------------------------------- |
| Números: 98, 15, 8, 98, 5, 47, 75, 13, 93, 75<br> 77, 84, 91, 58, 59, 13, 44,96, 35, 38. <br>x: 33 | Vetor A: 5, 8, 13, 15, 47, 75, 75, 93, 98, 98. <br>Vetor B: 13, 35, 38, 44, 58, 59,77,84,91,96<br>33 Não está em A.|
| Números: 77, 84, 91, 58, 59, 13, 44, 96, 35, 38<br>13, 18, -10, -7, 15, 17, 18,17, 17, -4.<br>x: 19| Vetor A: -10, -2, 0, 4, 9, 12, 13, 14, 19, 19. <br>Vetor B: -10, -7, -4, 13, 15, 17, 17, 17, 18, 18, 18. <br> 19 está em A na 10ª posição <br> O elemento na mesma posição em B é 18.*
