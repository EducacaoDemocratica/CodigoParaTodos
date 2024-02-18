# Exercício 59

[*Ver Algoritmo*](Algoritmo59.md)

*Um outro método de cifragem mais robusto é a Cifra de César. É um tipo de cifra de substituição na qual cada letra do texto é substituída por outra letra que se apresenta deslocada um número fixo de vezes da original. Por exemplo, com um deslocamento de três posições, A seria substituído por D, B se tornaria E, T se tornaria W, Y se tornaria B, Z se tornaria C, e assim por diante. Por exemplo, a palavra “MUSICA” com um deslocamento de 3 letras se torna “PXVLFD”. Faça um pseudocódigo que utilize a Cifra de César e que receba uma palavra de até 12 caracteres, dispostos em um vetor, um valor de deslocamento inteiro e positivo e a função de criptografar ou descriptografar a palavra. Na saída apresente a palavra cifrada ou decifrada. Se for necessário, use o caractere “@” para indicar o fim de uma palavra quando esta tiver menos caracteres que o total suportado. Serão cifrados ou decifrados APENAS os caracteres presentes no alfabeto, os demais caracteres não serão cifrados.*

**Entrada**

-A função f do sistema , uma palavra e o deslocamento d realizado.

**Saída**

- A palavra cifrada ou decifrada.

**Restrições**

- o sistema possui apenas duas funções: a de criptografia e a de descriptografia.
- a palavra deve conter no mínimo 6 letras e no máximo 15.
- o sistema não considera números, caracteres especiais ou outros, somente letras.
- o deslocamento não pode ser nulo ou, de alguma maneira, ineficiente.
 
**Exemplo**


| Entrada| Saída  |
|--------------------------|------------------------------------|
|f: “Criptografar”<br>palavra: “FLEXIBILIZAR”<br>d: 5|Palavra decifrada: CANUDO<br>Palavra cifrada: KQJCNGNQNEFW|
|f: “Descriptografar”<br>palavra: “UCA4QKI1”<br>d: 8|Palavra cifrada: UCAQKI<br>Palavra decifrada: MUSICA|
|f: “Criptografar”<br>palavra: “ESPELHO”<br>d: -3|Palavra decifrada: CANUDO<br>Palavra cifrada: BPMBIEL|
|f: “A”|Erro: essa função não existe.Selecione “criptografar” ou “descriptografar”:|
|f: “Criptografar”<br>palavra: “MARIA”|Erro: insira uma palavra de 6 a 15 caracteres:|
|f: “Descriptografar”<br>palavra: “SUSTENTABILIDADE”|Erro: insira uma palavra de 6 a 15 caracteres:|
|f: “Criptografar”<br>palavra: “NATUREZA”<br>d: 0|Erro: o deslocamento não pode ser ineficiente. Insira outro:|
|f: “Descriptografar”<br>palavra: “MAURÍLIO”<br> d: 52|Erro: o deslocamento não pode ser ineficiente. Insira outro:|