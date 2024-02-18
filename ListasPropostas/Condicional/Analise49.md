# Exercício 51

[**Ver Algoritmo**](Algoritmo51.md)

*Faça um pseudocódigo que receba um número inteiro positivo e informe se esse número pode ser um valor válido na base 2 que só utiliza os algarismos 0 e 1.*

**Entrada:**
- Um número inteiro n.

**Saída:**
- Se n é válido na base 2.

**Restrições:**
- n precisa ser positivo.# Exercício 49

[**Ver Algoritmo**](Algoritmo49.md)

*Faça um pseudocódigo para implementar o jogo jokenpô, ou pedra, papel e tesoura, contra o computador. O usuário escolherá sua opção e o computador também o fará de forma aleatória. O pseudocódigo determinará o ganhador e apresentará o placar do jogo. Ganha quem conseguir mais vitórias em uma rodada de 5 jogadas.*

**Entrada:**
- A escolha do jogador (pedra, papel ou tesoura).

**Saída:**
- O vencedor das cinco rodadas se houver.

**Restrições:**
- As escolhas só devem assumir “pedra”, “papel” ou “tesoura”.

*Nota: os dados do computador não são lidos, eles estão na entrada abaixo somente para facilitar a compreensão do que se pede*
**Exemplo:**
| Entrada | Saída |
| ------- | ----- |
| Computador: “Pedra”<br>Jogador: “Papel”;<br><br>Computador: “Tesoura”<br>Jogador: “Papel”;<br><br>Computador: “Pedra”<br>Jogador: “Pedra”;<br><br>Computador: “Tesoura”<br>Jogador: “Pedra”;<br><br>Computador: “Pedra”<br>Jogador: “Pedra”; |O jogador venceu. |
| Computador: “Tesoura”<br>Jogador: “Tesoura”;<br><br>Computador:“Pedra”<br>Jogador: “Papel”;<br><br>Computador: “Pedra”<br>Jogador: “Tesoura”;<br><br>Computador: “Papel”<br>Jogador: “Tesoura”;<br><br>Computador: “Papel”<br>Jogador: “Pedra”; | Empate.|
| Computador:"Papel"<br>Jogador:"A" | Erro: valor inválido para escolha |


**Exemplo:**
| Entrada | Saída |
| ------- | ----- |
| 0121 | Inválido na base 2. |
| 1101 | Válido na base 2. |
| -101 | Um número negativo foi encontrado. Insira outro número. |
