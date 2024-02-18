# Exercício 27

[*Ver Algoritmo*](Algoritmo27.md)

*A cifra de Vigenère é um método de criptografia que usa diferentes cifras de César baseadas em letras de uma senha. Durante mais de 300 anos esta cifra foi julgada inquebrável, mas Charles Babbage e Friedrich Kasinski, encontraram um modo de “quebrar” a cifra em meados do século XIX. A cifra consiste em uma tabela com o alfabeto escrito 26 vezes em diferentes linhas, cada linha contendo as letras deslocadas uma posição à frente em relação à linha anterior, representando as 26 possíveis cifras de César.*

*Veja a grade de Vigenère, conhecida também por tabula recta*


| | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| A | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |
| B | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A |
| C | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B |
| D | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C |
| E | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D |
| F | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E |
| G | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F |
| H | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G |
| I | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H |
| J | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I |
| K | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J |
| L | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K |
| M | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L |
| N | N | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M |
| O | O | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N |
| P | P | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O |
| Q | Q | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P |
| R | R | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q |
| S | S | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R |
| T | T | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S |
| U | U | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T |
| V | V | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U |
| W | W | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V |
| X | X | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W |
| Y | Y | Z | A | B | C | D | E | F | G | H | I | J | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |

*Para cifrar é escolhida uma "palavra-chave" onde cada letra vai indicar a linha a ser utilizada para cifrar ou decifrar uma letra da mensagem. Por exemplo, criptografar o texto: ATACARBASESUL ("atacar base Sul") Escolhendo a chave: LIMAO Repete-se a chave até ter o comprimento do texto a cifrar:*

| A | T | A | C | A | R | B | A | S | E | S | U | L |
|-|-|-|-|-|-|-|-|-|-|-|-|-|
| L | I | M | A | O | L | I | M | A | O | L | I | M |

*A primeira letra do texto, A, é cifrada usando o alfabeto na linha L, a primeira letra da chave. Basta olhar para a letra que está na linha que se inicia com L e coluna A na grade de Vigenère, e que é um L. Para a segunda letra do texto, T, usamos a segunda letra da chave, I, e procuramos a letra que está na linha I e coluna T, que é B, continuando sempre até obter cifrar todo o texto. A desencriptação é feita de modo inverso.*
*Texto: A T A C A R B A S E S U L<br>Chave: L I M A O L I M A O L I M<br>Saída: L B M C O C J M S S D C X*

*Faça um pseudocódigo que implemente a Cifra de Vigenère para textos e palavras chaves de até 15 caracteres. Receba o texto a ser modificado, a palavra chave e função de criptografar ou descriptografar a palavra. Na saída apresente a palavra cifrada ou decifrada. Se for necessário, use o caractere “@” para indicar o fim de uma palavra quando esta tiver menos caracteres que o total suportado. Serão cifrados ou decifrados APENAS os caracteres presentes no alfabeto, os demais caracteres não serão cifrados.*

**Entrada**

- A função f do sistema, o texto para modificação e palavra-chave.

**Saída**

- A palavra cifrada ou decifrada.

**Restrições**

- o sistema possui apenas duas funções: a de criptografia e a de descriptografia.
- a palavra deve conter no máximo 15.
- o sistema não considera números, caracteres especiais ou outros, somente letras.

 
**Exemplo**


| Entrada| Saída  |
|--------------------------|------------------------------------|
|f: “Criptografar”<br>palavra: “Visualg”<br>chave: “Programacao” |Palavra decifrada: VISUALG<br> Palavra cifrada: KZGARLS|
|f: “Descriptografar”<br>palavra: “Lbmcocjmssdcx”<br>chave: “Limao|Palavra cifrada: LBMCOCJMSSDCX<br>Palavra decifrada: ATACARBASESUL|
|f: X | Erro: essa função não existe. Selecione “criptografar” ou “descriptografar”:|
|f: “Criptografar”<br> palavra: “”|Erro: insira uma palavra de 6 a 15 caracteres:|
|f: “Descriptografar”<br>palavra: “Responsabilidade”| Erro: Insira uma palavra de 6 a 15 caracteres: |