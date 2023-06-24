# <h1 style="text-align:center">Machine Learning aplicado na analise de dados de EMG</h1>

# Abstract

A Pesquisa se desenvolve através de dados capturados via EMG (Eletromiografia), perfazendo de estatísticas
	e algorítimos de classificação.

# Keywords

EMG, Eletromiografia, Machine Learning, Estatísticas

# Introdução

## Introdução ao Machine Learning

Machine learing é um campo da ciência de dados devotado ao entendimento e a construção de métodos de aprendizagem, onde por meios de classificação dos dados, podemos prever dados futuros que se concentra no uso de dados e algoritmos para imitar a maneira como os humanos aprendem, melhorando gradualmente sua precisão.

## Introdução ao EMG

A Eletromiografia (EMG) é um exame que mede a atividade elétrica dos músculos em resposta de sua própria estimulação. Na medicina é utilizada para detectar anormalidades neuromusculares, o EMG mede os estímulos do músculo, contrações leves ou fortes, músculo em repouso, os músculos em repouso geralmente não apresentam atividade elétrica.


# Origem dos dados

A origem dos dados foram obtidos por eletromiografia, onde foram postos dois eletrodos no rosto, posicionados no corrugador do super cílio e no zigomático maior. Cada rotulo se divide um cinco expressões faciais, neutro, sorrindo, aberto, surpreso e grumpy, os dados da EMG variam em 0khz a 1khz.

## Conjunto dos dados

Os $dados \in \mathbb{R}^{NxP}$ onde suas dimensões, P são 2 preditores e N são 50000 observações, os $rotulos \in \mathbb{R}^{NxC}$ onde N é são amostras 5 e C são 50000 classes.

A rotina de medição foi 1000 amostras de cada expressão facial repetidas 10 vezes resultando em 50000 amostras.

# Fundamentação teorica

## Classificadores de dados matriciais

Classificadores de dados matriciais, são ótimos para grandes volumes de dados como este em que está sendo discutido, trazendo confiabilidade, velocidade e simplicidade nos modelos.

## OLS (Ordinary Least Squares)

O primeiro modelo a ser discutido, OLS (Ordinary Least Squares) para o português MQO (Mínimos quadrados ordinários), é uma técnica de estimação dos coeficientes de uma regressão linear aos quais descreve o relacionamento com uma ou mais variáveis sendo elas quantitativas ou não.

O modelo é dado pela seguinte equação linear:

$$\beta = (X^{T}X)^{-1}X^{T}y$$

onde X, é a matriz de dados e y é os rotulos

## Regularização por Tikhonov

Um método usado para evitar mau-condicionamento. Em geral, o método fornece maior eficiência em problemas de estimativa de parâmetros em troca de uma quantidade tolerável de viés

Representada somente pela adição do termo de regularização $\lambda$ onde varia de $0 \leqslant  \lambda \leqslant 1$ multiplicado por uma matriz identidade $I \in \mathbb{R}^{PxP}$ e somada a primeira parte da equação 

Depois da adição $\lambda I$ ganha a seguinte forma:

$$\beta = (X^{T}X + \lambda I)^{-1}X^{T}y$$

## PDF (Probability Density Function)

A PDF (Probability Density Function), para o português FDP (Função de Densidade e Probabilidade), também conhecida como classificador Navie Bayers, distribuição gaussiana, multivariada distribuição normal, ou somente como normal, método de classificação a qual base-a-se na probabilidade da variável está dentro da integral.

PDF, Navie Bayes, Distribuição Gaussiana:
$$p(x|\mu,\sigma) = \frac{1}{\sqrt{2\pi\sigma^2}}\exp{\frac{-(x - \mu)^2}{2\sigma^2}}$$

Multivariada Distribuição Normal:
$$p(x|\mu,\Sigma) = \frac{1}{\sqrt{(2\pi)^d}|\Sigma|}\exp{-\frac{1}{2}(\textbf{x} - \mu)^T\Sigma^{-1}(\textbf{x} - \mu)}$$
onde $\mu$ é o vetor de médias, \textbf{x} matriz de dados separado por classe, $\Sigma$ representa a matriz de covariância.

## Multivariada Distribuição Normal regularizada por Friedman

Método usado para melhorar a degradação da função discriminante (5) para dados de alta-dimensibilidade, precisão em poucos dados ou não invertibilidade da matriz.

A função discriminante é dada pela seguinte equação:
$$g_{i}(\textbf{x}_{n}) = (\textbf{x}_{n} - \mu_{i})^T\Sigma^{-1}(\textbf{x}_{n} - \mu_{i})$$
Tal método faz combinação linear da matriz agregada das classes:
$$\Sigma_{agregada} = \frac{n_{1}}{N}\Sigma_{1} + \frac{n_{2}}{N}\Sigma_{2} + ... + \frac{n_{c}}{N}\Sigma_{c} $$
$$= P(y_{1})\Sigma_{1} + P(y_{2})\Sigma_{2} + ... + P(y_{c})\Sigma_{c}$$
$$= \sum^{C}_{i=1} P(y_{i})\Sigma_{i}$$
Regularização por Friedman:
$$\Sigma^{\lambda}_{i} = \frac{(1 - \lambda)(n_{i} \cdot \Sigma_{i}) + (\lambda \cdot N \cdot \Sigma_{agregada})}{(i - \lambda)n_{i} + \lambda \cdot N}$$
De maneira que $\lambda$ receba $0 \leqslant \lambda \leqslant 1$ e resulte em uma nova matriz de covariância $\Sigma$.

## Multivariada Distribuição Normal Pooled

Este método faz uma abordagem com a matriz de covariância agregada $\Sigma_{agregada}$ (6).


Todos esses métodos dependem do resultado do calculo da matriz de covariância $\Sigma$. 



