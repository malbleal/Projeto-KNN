# Projeto-KNN
Primeiro projeto do curso ADA - Dados


O KNN (K-Nearest Neighbors) é um algoritmo de aprendizado de máquina supervisionado utilizado tanto para classificação quanto para regressão. 
A ideia básica por trás do KNN é atribuir uma classe a um ponto de dados com base nas classes dos pontos vizinhos mais próximos a ele.

O funcionamento é simples: dado um conjunto de dados de treinamento com rótulos conhecidos, o algoritmo calcula a distância entre um ponto de
teste (sem rótulo) e todos os pontos de treinamento. Os pontos mais próximos ao ponto de teste são selecionados (os "vizinhos mais próximos"),
e a classe mais frequente entre esses vizinhos é atribuída ao ponto de teste.

Tendo isso em vista, a escolha do melhor 'K' é extremamente necessária para o código fluir de maneira certa e precisa.
Como fizemos esse projeto em grupo, aqui em baixo deixarei disponibilizado algumas conclusões sobre o melhor 'K'.


Mauricio.
---------------------------

	K = 3 
	10 0 0
	0 10 0
	0  2  8

Essa é nossa matriz em relação ao gabarito que o professor disponibilizou, analisando essas duas matrizes é nítido que 
nosso modelo está com dificuldades para acertar a previsão de quem tem o modelo de investimento agressivo, 
independentemente do tamanho do K. 
Isso poder ser dado por algum erro no código, mas não sei identificar se é de implementação ou de lógica.

quanto maior o K, nosso código tem dificuldades para acertar os indivíduos com o perfil de investimento agressivo

fiz um teste só por desencargo com k=1 e a matriz ficou desta forma:

	K = 1
	10 0 0
	0 10 0
	0  1  9

(com k=2 a matriz se mantém a mesma de k=3)

	K = 2|3
	10 0 0
	0 10 0
	0 02 8


(com k=4 ja perdemos eficiência na hora de identificarmos os 'Agressivos')

	K = 4 
	10 0 0
	0 10 0
	0  3  7

Tendo isso em vista, o melhor K para essa situação é k=3, pois minimiza os erros em Agressivo, visto que por o k=1 não existe comparação de vizinhoS mas sim de vizinhO. 


Daniel.
---------------------------
. Quando k = 2:
. Dos 40 conservadores, ele acertou a classificação de todos (100% de precisão)
. Dos 40 moderados, ele acertou a classificação de todos (100% de precisão)
. Dos 40 agressivos, ele acertou a classificação de 38 (95% de precisão)

. Quando k = 3:
. Dos 40 conservadores, ele acertou a classificação de todos (100% de precisão)
. Dos 40 moderados, ele acertou a classificação de todos (100% de precisão)
. Dos 40 agressivos, ele acertou a classificação de 36 (90% de precisão)
. TOTAL: acerta a classificação de 96,66%. k=3 é o melhor cenário verificado.

. Quando k = 4:
. Dos 40 conservadores, ele acertou a classificação de todos (100% de precisão)
. Dos 40 moderados, ele acertou a classificação de todos (100% de precisão)
. Dos 40 agressivos, ele acertou a classificação de 33 (82,50% de precisão)

. Quando k = 5:
. Dos 40 conservadores, ele acertou a classificação de todos (100% de precisão)
. Dos 40 moderados, ele acertou a classificação de todos (100% de precisão)
. Dos 40 agressivos, ele acertou a classificação de 30 (75% de precisão)

. Quando k = 6:
. Dos 40 conservadores, ele acertou a classificação de todos (100% de precisão)
. Dos 40 moderados, ele acertou a classificação de todos (100% de precisão)
. Dos 40 agressivos, ele acertou a classificação de 27 (67,50% de precisão)


. Quando k = 7:
. Dos 40 conservadores, ele acertou a classificação de todos (100% de precisão)
. Dos 40 moderados, ele acertou a classificação de todos (100% de precisão)
. Dos 40 agressivos, ele acertou a classificação de 26 (65% de precisão)

---------------------------
