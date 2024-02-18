# Exercício 57

[*Ver Algoritmo*](Algoritmo57.md)

*Você já jogou Termo? Nesse jogo são dadas 6 chances para o jogador descobrir uma palavra secreta de 5 letras. Se em alguma das 6 palavras arriscadas tiver alguma letra da palavra secreta, mas fora do lugar, essa letra ficará em minúscula. Se na palavra arriscada tiver alguma letra da palavra secreta no seu devido lugar, essa letra ficará em maiúsculo. No lugar das demais letras ficará o símbolo *. Faça um pseudocódigo que simule o Termo.*

*Você pode utilizar a função “aleatório” do Visualg, porém é mais elegante utilizar palavras gravadas em um arquivo de texto. Pesquise sobre o comando “arquivo” do Visualg. Pesquise também sobre o comando asc e o padrão ASCII para a representação de letras.*


**Entrada**

- 6 tentativas (palavras de 5 letras) do usuário.

**Saída**

- A cada tentativa mostrar os acertos do usuário e no fim a palavra secreta.

**Restrições**

- Cada tentativa deve conter somente letras, sem caractere vazio ou algum outro.
- cada tentativa deve conter somente 5 dígitos.
- evite caracteres especiais.
 
**Exemplo**
*Nota: a palavra sorteada não é lida, ela está na entrada abaixo somente para facilitar a compreensão do que se pede.*

| Entrada| Saída  |
|--------------------------|------------------------------------|
|palavra sorteada: Vulgo<br>1ª tentativa: AREIA<br>2ª tentativa: BOLSO<br>3ª tentativa: SOLTO<br>4ª tentativa: AMIGO<br>5ª tentativa: PULGO<br>6ª tentativa: SULGO|//após a 1ª tentativa<br>AREIA -> #####<br>//após a 2ª tentativa<br>BOLSO -> #oL#O<br>//após a 3ª tentativa<br>SOLTO -> #oL#O<br>//após a 4ª tentativa<br>AMIGO -> ###GO<br>//após a 5ª tentativa<br>PULGO -> #ULGO<br>//após a 6ª tentativa<br>FULGO -> #ULGO<br>Não foi dessa vez...<br>Palavra sorteada: VULGO.|
|palavra sorteada: Sobre<br>1ª tentativa: AREIA<br>2ª tentativa: RESTO<br>3ª tentativa: SOBRE|//após a 1ª tentativa<br>AREIA -> #re##<br>//após a 2ª tentativa<br>RESTO -> res#o<br>//após a 3ª tentativa<br>Parabéns!!! Você acertou.<br>Palavra sorteada: SOBRE.|
|palavra sorteada: Temor<br>1ª tentativa: AREI<br>loop: AREIAS<br>loop: SEÇÃO<br>loop: MACA1<br>loop: SECAO<br>2ª tentativa: PEROS<br>3ª tentativa: RESTO<br>4ª tentativa: METOR<br>5ª tentativa: TEMOR<br>|//após a 1ª tentativa<br>Insira uma palavra de 5 caracteres:<br>//loop<br>Insira uma palavra de 5 caracteres:<br>//loop<br>Insira somente letras:<br>//loop<br>Insira somente letras:<br>//loop<br>SECAO -> #E##o<br>//após a 2ª tentativa<br>PEROS -> #ErO#<br>//após a 3ª tentativa<br>RESTO -> rE#to<br>//após a 4ª tentativa<br>METOR -> mEtOR<br>//após a 4ª tentativa<br>Parabéns!!! Você acertou.<br>Palavra sorteada: TEMOR.<br>|