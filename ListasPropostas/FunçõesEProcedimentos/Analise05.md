# Exercício 05

[**Ver Algoritmo**](Algortimo05.md)

*A análise combinatória é um ramo da matemática que estuda como elementos
em um conjunto podem se combinar. Uma combinação possível é a permutação que
leva em conta a mudança de posição dos elementos do grupo, formando uma nova
organização. A fórmula para saber o número de combinações possíveis em um
conjunto dado é:*



$$P_n^{\alpha,\beta,\gamma} = \frac{n!}{\alpha!\beta!\gamma!}$$




*Onde P é a permutação de n elementos com α repetições de um elemento, β
repetições de outro elemento e
sucessivamente.
γ repetições de outro elemento, e assim
As repetições não se limitam a 3 apenas, pode ser de tantas quanto forem, a mais ou a menos.
Por exemplo:*

*- Permutações com a palavra PERNAMBUCO: P = 10! (não há letras que se
repetem);*
*- Permutações com a palavra BATATA: P = 6! / (3! x 2!) (possui 3 letras A e
2 letras T)/*
*- Permutações com a palavra CONSTITUCIONALISSIMAMENTE: P = 25! / (2!
x 2! x 3! x 3! x 3! x 4! x 3! x 2! x 2!)*

*Faça um pseudocódigo em Visualg, usando módulos, que recebe uma palavra
qualquer de ATÉ 46 letras e calcule as permutações possíveis com as letras que a
compõe.
Você conhece a maior palavra da língua portuguesa registrada no dicionário?*



**Entrada**

- Uma palavra p.


**Saída**

- As permutações possíveis com a palavra p.
  
**Restrições**

- a palavra deve ser preenchida corretamente sem espaços vazios;
- a palavra pode ter até 46 letras.

**Exemplo**

| Entrada | Saída | 
|-|-|
| “Responsabilidade|”Permutações com a palavra<BR> RESPONSABILIDADE: 16!/( 2! X 2! X 2! X 2! X2!)<BR>Um total de 653837184000 resultados.|
|“Tomate”|Permutações com a palavra<BR> TOMATE: 6!/( 2!)<BR>Um total de 360 resultados.|
|“ ”|Erro: não preencha com espaços vazios.<BR>Insira outra palavra|