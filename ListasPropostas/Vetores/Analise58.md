# Exercício 58

[*Ver Algoritmo*](Algoritmo58.md)

*Criptografia refere-se à construção e análise de protocolos que impedem terceiros, ou o público, de lerem mensagens privadas. Uma técnica de criptografia é a cifragem, o processo de conversão de um texto em uma forma compreensível para um código cifrado, apresentado de forma não compreensível. A decifragem é o processo contrário, aquele que recupera o texto original a partir de um texto cifrado.Um método clássico é a cifra JULIO CESAR, onde uma palavra, por exemplo, MUSICA, é cifrada, substituindo qualquer caractere que houver na palavra um correspondente na cifra. Por exemplo:*

*Palavra: MUSICA	M -> Não tem na cifra, se mantém*
*Cifra:U -> troca pela letra E, pois, U ocupa em*
*JULIO mesma posição que E em CESAR*
*J U L I O*
*C E S A R*
*S -> troca pela letra L*
*I -> troca pela letra A*
*C -> troca pela letra J*
*A -> troca pela letra I*
*MUSICA -------> MELAJI*

*Faça um pseudocódigo que utilize o método JULIO CESAR e que receba uma palavra de 6 a até 15 caracteres, dispostos em um vetor, e a função de criptografar ou descriptografar a palavra. Na saída apresente a palavra cifrada ou decifrada. Se for necessário, use o caractere “@” para indicar o fim de uma palavra quando esta tiver menos caracteres que o total suportado. Serão cifrados ou decifrados APENAS os caracteres presentes no alfabeto, os demais caracteres não serão cifrados.*

**Entrada**

-A função f do sistema e uma palavra.

**Saída**

- A palavra cifrada ou decifrada.

**Restrições**

- o sistema possui apenas duas funções: a de criptografia e a de descriptografia.
- a palavra deve conter no mínimo 6 letras e no máximo 15.
- o sistema não considera números, caracteres especiais ou outros, somente letras.
 
**Exemplo**


| Entrada| Saída  |
|--------------------------|------------------------------------|
|f: “Criptografar”<br>palavra: “Ca nu2do#”|Palavra decifrada:CANUDO<br>Palavra cifrada: JINEDR|
|f: “Descriptografar”<br>palavra: “Bajajsuti”|Palavra cifrada: BAJAJSUTI<br>Palavra decifrada: BICICLETA|
|f: “X”|Erro: essa função não existe.<br>Selecione “criptografar” ou “descriptografar”:|
|f: “Criptografar”<br>palavra: “João”|Erro: insira uma palavra de 6 a 15 caracteres:|
|f: “Descriptografar”<br>palavra: “Responsabilidade”|Erro: insira uma palavra de 6 a 15 caracteres:|