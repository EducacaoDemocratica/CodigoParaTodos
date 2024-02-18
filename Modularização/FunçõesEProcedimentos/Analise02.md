# Exercício 02

[**Ver Algoritmo**](Algoritmo02.md)

*Faça um pseudocódigo que utilize funções para converter uma temperatura em graus Celsius (C) para Kelvin (K), Réaumur (Re), Rankine (Ra) e Fahrenheit (F). A fórmula de conversão de cada temperatura é:*
- \(F = C * 1.8 + 32\)
- \(K = C + 273.15\)
- \(Re = C * 0.8\)
- \(Ra = C * 1.8 + 32 + 459.67\)

*Considere apenas as temperaturas em Celsius maiores que o zero absoluto (0 Kelvin).*

**Entrada**
- Uma temperatura em graus Celsius.

**Saída**
- A temperatura em Celsius convertida para as escalas Kelvin, Réaumur, Rankine e Fahrenheit.

**Restrições**
- A temperatura em Celsius não deve ser menor que -273.15.

**Exemplo**

| Entrada | Saída |
|---------|-------|
| 0       | Temperatura em Celsius: 0º C.<br>Temperatura em Kelvin: 273.15K.<br>Temperatura em Réaumur: 0º Re.<br>Temperatura em Rankine: 491.67Ra.<br>Temperatura em Fahrenheit: 32º F. |
| 37.778  | Temperatura em Celsius: 37.778º C.<br>Temperatura em Kelvin: 310.928K.<br>Temperatura em Réaumur: 30.2224º Re.<br>Temperatura em Rankine: 559.6704Ra.<br>Temperatura em Fahrenheit: 100º F. |
| -274    | Erro: insira um valor maior que -273.15: |
