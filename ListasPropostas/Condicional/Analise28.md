# Exercício 28

[**Ver Algoritmo**](Algoritmo28.md)

*Jogo de palitinho é um jogo muito comum onde os participantes recebem, cada um, 5 palitos e colocam uma quantidade qualquer de palitos na mão direita, indo dos 5 palitos ou até nenhum. Todos mostram a mão direita fechada e cada um tenta adivinhar a soma dos palitos que aparecerão quando todos abrirem a mão direita. Ganha aquele que acertar a quantidade. Você escolhe um valor entre 0 e 5 e o adversário também escolhe um valor aleatório entre 0 e 5. Em seguida, você coloca a sua sugestão de soma e o adversário também apresenta a sugestão de soma dele. Faça um pseudocódigo que permita você jogar palitinho com o computador. É possível dar algum grau de “inteligência” para seu algoritmo, onde a sugestão do computador nunca será menor que o valor de palitinhos que ele escolheu. Pesquise sobre a função randi() do Visualg.*

**Entrada**
- Quantidade dos palitinhos do jogador (p) e a sugestão de soma (s).

**Saída**
- O vencedor do jogo do palitinho.

**Restrições**
- Ambos os valores não podem ser números negativos.
- O número de palitinhos p não deve ser maior que 5.
- A sugestão de soma s não deve ser maior que 10.

**Exemplos**

Nota: os dados do computador não são lidos, eles estão na entrada abaixo somente para facilitar a compreensão do que se pede.

| Entrada                                             | Saída                         |
| ----------------------------------------------------| ------------------------------|
| Palitinhos do computador: 0<br>Soma do computador: 3<br><br>Palitinhos do usuário: 1<br>Soma do usuário: 3   | Empate.                       |
| Palitinhos do computador: 3<br>Soma do computador: 5<br><br>Palitinhos do usuário: 0<br>Soma do usuário: 3  | O jogador venceu.             |
| Palitinhos do computador: 2<br>Soma do computador: 2<br><br>Palitinhos do usuário: 10<br>Soma do usuário: 10  | Erro: quantidade de palitinhos negativa ou maior que 5. |
| Palitinhos do computador: 1<br>Soma do computador: 2<br><br>Palitinhos do usuário: 5<br>Soma do usuário: 11  | Erro: soma negativa ou maior que 10. |

