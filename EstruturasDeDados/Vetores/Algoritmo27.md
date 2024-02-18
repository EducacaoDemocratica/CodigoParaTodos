# Exercício 27

[**Ver Análise**](Analise27.md)

```markdown

Algoritmo "Q27 - exVetor"

Var
	i, lsup: inteiro
	v: vetor [1..15] de real
Inicio
	lsup <- 15
	para i de 1 ate lsup faca
    		escreva("Insira o", i, "º número: ")
    		leia(v[i])
    			enquanto ((v[i] <= -6) ou (v[i] > 3)) faca
        			escreva("Insira um número do intervalo ]-6, 3]: ")
				leia(v[i])
			fimenquanto
	fimpara
	escreval
	para i de 1 ate lsup faca
    		se (i = lsup) entao
        		escreval(v[i], ".")
	    senao
    		    escreva(v[i], ",")
	    fimse
	fimpara
Fimalgoritmo