# <h1 style="text-align:center">Busca Meta-heurística e Algoritmos Genéticos para Problemas de Otimização</h1>

# Abstract


Os algoritmos de busca meta-heurística têm recebido grande atenção na resolução de problemas de otimização complexos. Entre essas meta-heurísticas, os algoritmos genéticos (GAs) têm se mostrado eficazes na busca de soluções de alta qualidade em uma ampla gama de domínios. Este artigo apresenta um estudo abrangente da aplicação de técnicas de busca meta-heurística, com foco em algoritmos genéticos, para problemas de otimização. O objetivo é analisar a eficácia e eficiência dos GAs na solução de diferentes tipos de problemas de otimização, incluindo problemas combinatoriais, contínuos e multiobjetivo.

# Keywords
Meta-heurística, Algoritmos genéticos, Otimização, Problemas combinatoriais, Problemas contínuos, Problemas multiobjetivo

# Introdução

## Busca/Otimização Meta-Heurística

A busca meta-heurística difere dos métodos tradicionais de otimização, como a programação linear ou a busca exaustiva, ao explorar estratégias de busca não determinísticas e heurísticas, que podem escapar de mínimos locais e buscar soluções melhores em um espaço de busca mais amplo. Essas técnicas são particularmente adequadas para problemas em que a função objetivo não é facilmente diferenciável ou quando o espaço de busca é grande e não pode ser totalmente explorado em tempo viável.

As técnicas de busca meta-heurística têm desempenhado um papel fundamental na resolução de problemas complexos em diversas áreas, desde otimização combinatória até aprendizado de máquina. Essas abordagens fornecem métodos eficientes e flexíveis para encontrar soluções aproximadas ou ótimas em espaços de busca.

## Algorítimos Genéticos (GA)

Algoritmos genéticos são uma classe de algoritmos de otimização inspirados no processo de evolução biológica. Eles são usados para resolver problemas complexos de otimização e busca, onde uma solução ideal é encontrada dentro de um espaço de soluções possíveis.

Esses algoritmos foram desenvolvidos com base na teoria da evolução de Darwin, que postula que as espécies evoluem ao longo do tempo por meio de um processo de seleção natural, no qual os indivíduos mais aptos têm maior probabilidade de sobreviver e se reproduzir, transmitindo suas características vantajosas para as gerações futuras. 

# Fundamentação Teorica

## Hill Climbing (Subida de encosta)

O Hill Climbing, também conhecido como subida de encosta, é um algoritmo de otimização heurística usado para encontrar soluções aproximadas para problemas de maximização ou minimização. Ele é um exemplo de busca local que tenta melhorar iterativamente uma solução por meio de movimentos em direção a soluções vizinhas que possuem um valor de função objetivo melhor.

<ul>
    <li>
        Inicializada uma solução inicial aleatória ou determinística.
    </li>
    <li>
        Avaliação do valor da função objetivo para a solução inicial.
    </li>
    <li>
        Repetições até que uma condição de parada seja atingida:
    </li>
    <li>
        a. Geração de uma solução vizinha da solução atual.
    </li>
    <li>
        b. Avaliação do valor da função objetivo para cada solução vizinha.
    </li>
    <li>
        c. Se a solução vizinha tiver um valor de função objetivo melhor que o da solução atual, mova-se para essa solução vizinha.
    </li>
    <li>
        d. Se nenhuma solução vizinha tiver um valor de função objetivo melhor, continua com a solução atual.
    </li>
    <li>
        Finaliza com a solução encontrada e aproximada para o problema.
    </li>
</ul>

O Hill Climbing pode ser usado em uma variedade de problemas, desde que seja possível definir uma função objetivo para avaliar a qualidade das soluções. No entanto, o algoritmo pode ficar preso em ótimos locais, onde não é possível encontrar soluções melhores.

## Busca Local Aleatória (Local Random Search) (LRS)

A busca local aleatória é uma técnica de busca heurística que faz uso de movimentos aleatórios para explorar o espaço de soluções de um problema. Ao contrário do algoritmo Hill Climbing, que sempre se move para soluções vizinhas com valores de função objetivo melhores, a busca local aleatória permite movimentos para soluções piores, com o objetivo de evitar ficar preso em ótimos locais e explorar diferentes regiões do espaço de soluções.

<ul>
    <li> 
        Inicializada uma solução inicial aleatória ou determinística.
    </li>
    <li>
    Avaliação do valor da função objetivo para a solução inicial.
    </li> 
    <li>
        Repetição até que uma condição de parada seja atingida:
    </li> 
    <li>
        a. Geração de uma nova solução vizinha aleatória.
    </li>
    <li>
        b. Avaliação do valor da função objetivo para a nova solução vizinha.
    </li>
    <li>
        c. Se a nova solução vizinha tiver um valor de função objetivo melhor que o da solução atual, mova-se para essa nova solução.
    </li>
    <li>
        d. Se a nova solução vizinha tiver um valor de função objetivo pior, mova-se para ela com uma probabilidade determinada (Probabilidade Gaussiana).
    </li>
    <li>
        Finaliza com a melhor solução encontrada durante a execução como a solução aproximada para o problema.
    </li>
</ul>

A busca local aleatória oferece uma abordagem mais exploratória em relação ao Hill Climbing, permitindo que o algoritmo escape de ótimos locais, mas também pode levar mais tempo para convergir para uma solução de alta qualidade. Ela é particularmente útil em problemas onde o espaço de soluções é complexo e irregular.

## Busca Global Aleatória (Global Random Search) (GRS)

A busca global aleatória, também conhecida como busca aleatória, é uma técnica de busca heurística que explora aleatoriamente o espaço de soluções em busca da solução ótima ou próxima ótima de um problema. Ao contrário das técnicas de busca local, como o Hill Climbing, que se concentram em explorar soluções vizinhas, a busca global aleatória faz uma busca ampla e aleatória em todo o espaço de soluções.

<ul>
    <li>
        Definição de um número máximo de iterações ou tempo de execução
    </li>
    <li>
        Inicialização de uma solução aleatória.
    </li> 
    <li>
        Avaliação do valor da função objetivo para a solução atual.
    </li>
    <li>
        Atribuição da melhor solução encontrada como a solução atual.
    </li>
    <li>
        Repetição até atingir o número máximo de iterações ou tempo de execução:
    </li>
    <li>
        a. Geração de uma nova solução aleatória.
    </li>
    <li>
        b. Avaliação do valor da função objetivo para a nova solução.
    </li>
    <li>
        c. Se a nova solução tiver um valor de função objetivo melhor que a melhor solução encontrada, atualiza a melhor solução.
    </li> 
    <li>Finaliza com a melhor solução encontrada como a solução aproximada para o problema.</li>
</ul>

A busca global aleatória é uma abordagem simples e direta, mas pode ser computacionalmente intensiva, especialmente para problemas com um grande espaço de soluções. Devido à sua natureza aleatória, não há garantia de que a solução ótima seja encontrada. No entanto, a busca global aleatória pode ser útil em problemas complexos, onde o espaço de soluções não é bem conhecido e técnicas de busca mais sofisticadas podem ser ineficientes.


## Têmpera Simulada (Simulated Annealing)

A têmpera simulada, também conhecida como simulated annealing em inglês, é um algoritmo de otimização que foi inspirado pelo processo físico de têmpera do metal. É uma técnica de busca heurística que permite movimentos para soluções piores com uma certa probabilidade, com o objetivo de escapar de ótimos locais e explorar diferentes regiões do espaço de soluções.

<ul>
    <li>
        Inicialização de uma solução inicial aleatória ou determinística.
    </li>
    <li>
        Avaliação do valor da função objetivo para a solução inicial.
    </li>
    <li>
        Definição de uma a temperatura inicial e a temperatura final.
    </li>
    <li>
        Repetição até que a temperatura atual atinja a temperatura final:
    </li>
    <li>
        a. Repetição até que um critério de parada seja atingido:
    </li>
    <li>
        i. Geração de uma nova solução vizinha.
    </li>
    <li>
        ii. Avaliação do valor da função objetivo para a nova solução vizinha.
    </li>
    <li>
        iii. Calculo da variação de energia entre a nova solução e a solução atual.
    </li>
    <li>
        iv. Se a variação de energia for negativa, aceite a nova solução como a solução atual.
    </li>
    <li>
        v. Se a variação de energia for positiva, aceite a nova solução com uma probabilidade determinada (probabilidade Gaussiana) e atualize a solução atual.
    </li>
    <li>
        b. Redução da temperatura atual de acordo com alguma estratégia de resfriamento.
    </li>
    <li>
        Finaliza com a melhor solução encontrada durante a execução como a solução aproximada para o problema.
    </li>
</ul>

O algoritmo de têmpera simulada utiliza uma estratégia de resfriamento gradual, em que a probabilidade de aceitar soluções piores diminui à medida que o algoritmo progride. Isso é análogo ao resfriamento lento de um material durante o processo de têmpera, em que a taxa de resfriamento é reduzida gradualmente.

A chave para o sucesso da têmpera simulada está na estratégia de resfriamento, pois é responsável por controlar a exploração inicial do espaço de soluções (quando a temperatura é alta) e a exploração mais localizada e refinada (quando a temperatura é baixa). A temperatura inicial e a taxa de resfriamento são ajustadas para se adequarem ao problema específico.

A têmpera simulada é particularmente útil para problemas onde o espaço de soluções possui muitos ótimos locais e pode ser difícil encontrar a solução globalmente ótima. Ao permitir movimentos para soluções piores, a têmpera simulada evita ficar presa em ótimos locais e tem a capacidade de encontrar soluções melhores ou até mesmo a solução ótima global, dependendo da qualidade da função objetivo e dos parâmetros ajustados corretamente.

## Algorítimos Genéticos (GA's)

Algoritmos genéticos são técnicas de busca e otimização inspiradas na evolução biológica. Eles são usados para resolver problemas de otimização, onde o objetivo é encontrar a melhor solução possível em um espaço de soluções.

O funcionamento básico de um algoritmo genético envolve a manipulação de uma população de indivíduos, onde cada indivíduo representa uma solução para o problema em questão. Cada indivíduo é codificado em um conjunto de genes, que representam características ou parâmetros da solução.



Inicialização:

Gere uma população inicial de indivíduos de forma aleatória ou determinística.

Avaliação:

Calcule o valor de aptidão (fitness) para cada indivíduo da população. A aptidão é uma medida de quão boa é a solução representada pelo indivíduo.

Seleção:

Selecione indivíduos da população atual com base em sua aptidão. Indivíduos com maior aptidão têm maior probabilidade de serem selecionados.
Existem várias estratégias de seleção, como seleção por roleta, torneio ou classificação.

Reprodução:

Crie novos indivíduos por meio de operadores genéticos, como cruzamento (recombinação) e mutação.
O cruzamento envolve a combinação de genes de dois ou mais indivíduos selecionados, gerando descendentes que herdam características dos pais.
A mutação introduz pequenas alterações aleatórias nos genes dos indivíduos selecionados.

Substituição:

Substitua a população anterior pela nova população gerada através da reprodução.
Pode-se usar várias estratégias de substituição, como substituição geracional (a nova população substitui completamente a anterior) ou substituição por elitismo (alguns dos melhores indivíduos da população anterior são mantidos na nova população).


O objetivo do algoritmo genético é evoluir a população de forma iterativa, de modo que as soluções melhores tenham maior probabilidade de serem selecionadas, reproduzidas e transmitidas para as gerações futuras. Com o tempo, espera-se que a população evolua em direção a soluções de maior qualidade.

### Problema do Caixeiro Viajante

O Problema do Caixeiro Viajante é um dos problemas mais conhecidos e estudados no campo da otimização combinatória. Ele desafia a encontrar a rota mais curta que um caixeiro viajante deve percorrer para visitar um conjunto de cidades uma vez e retornar à cidade de origem.

A tarefa do caixeiro viajante é encontrar a rota que minimize a distância total percorrida, considerando que cada cidade deve ser visitada exatamente uma vez e que o caixeiro deve retornar à cidade de partida. Esse problema é classificado como NP-difícil, o que significa que não existem algoritmos conhecidos que possam resolvê-lo em tempo polinomial para um número arbitrário de cidades.

Uma abordagem comum para resolver o Caixeiro Viajante é usar algoritmos de busca heurística, como os algoritmos genéticos que mencionei anteriormente.

### 8 Rainhas

O problema das 8 rainhas é um famoso desafio de colocação de peças de xadrez em um tabuleiro de xadrez 8x8, onde o objetivo é posicionar oito rainhas no tabuleiro de forma que nenhuma rainha seja capaz de capturar outra rainha. Isso significa que nenhuma rainha pode estar na mesma linha, coluna ou diagonal de outra rainha.

A solução para o problema das 8 rainhas envolve encontrar uma disposição das oito rainhas no tabuleiro que atenda a todas as restrições mencionadas. É um problema clássico de busca e otimização combinatória.

Para resolver o problema das 8 rainhas, existem várias abordagens possíveis, incluindo algoritmos exatos, como a busca em profundidade com retrocesso (backtracking), e algoritmos heurísticos, como algoritmos genéticos ou busca local.

# Fundamentação teorica

## Hill Climbing

<pre>

    Algorithm 1 Hill Climbing
    
    Require: x1, x2, f , e, maxit, maxn
    
    x0 ← ? < x0 < ?
    x1 ← ? < x1 < ?

    xbest ← x0, x1
    fbest ← f (xbest)
    
    melhoria ← False
    i ← 0
    
    while i < maxit and melhoria do
        j ← 0
        while j < maxn do
            melhoria ← False
            y ← unif orm(xbest − e, xbest + e)
            F ← f (y)
            if F > fbest then
                xbest ← y
                xbest ← F
                melhoria ← True
                break
            end if
            j ← j + 1
        end while
        i ← i + 1
    end while

</pre>

## Busca Local Aleatoria

<pre>
    Algorithm 2 Busca Local Aleatória
    Require: x1, x2,xl, xu, f , σ, maxit, maxn
    x0 ← ? < x0 < ?
    x1 ← ? < x1 < ?
    σ ← ? < ≈ < ?
    xl ← min(x0, x1)
    xu ← max(x0, x1)
    xbest ∼ unif orm(xl, xu)
    fbest ← f (xbest)
    i ← 0
    while i < maxit do
        n ← normal(0, σ)
        y ← xbest + n
        if y > xu then
            y ← xu
        end if
        if y < xl then
            y ← xl
        end if
        F ← f (y)
        if F > fbest then
            xbest ← y
            xbest ← F
        end if
        j ← j + 1
    end while

</pre>

## Busca Global Aleatória

<pre>
    Algorithm 3 Busca Global Aleat ́oria
    Require: x1, x2,xl, xu, f , maxit, maxn
    x0 ← ? < x0 < ?
    x1 ← ? < x1 < ?
    xl ← min(x0, x1)
    xu ← max(x0, x1)
    xbest ∼ uniform(xl, xu)
    fbest ← f (xbest)
    i ← 0
    while i < maxit do
        y ∼ uniform(xl, xu)
        F ← f (y)
        if F > fbest then
            xbest ← y
            xbest ← F
        end if
        j ← j + 1
    end while

</pre>

## Tempera Simulada

<pre>
    Algorithm 4 Simulated Annealing (Tempera Simulada)
    Require: x1, x2,xl, xu, f , σ, T , maxit, maxn
    x0 ← ? < x0 < ?
    x1 ← ? < x1 < ?
    σ ← ? < ≈ < ?
    T ← 100
    xl ← min(x0, x1)
    xu ← max(x0, x1)
    xbest ∼ uniform(xl, xu)
    fbest ← f(xbest)
    i ← 0
    while i < maxit do
        n ← normal(0, σ)
        y ← xbest + n
        if y > xu then
            y ← xu
        end if
        if y < xl then
            y ← xl
        end if
        F ← f (y)
        if F > fbest then
            xbest ← y
            xbest ← F
        else if exp −{f(xi) − f (xj)}/T >= uniform(0, 1) then
            xbest ← y
            xbest ← F
        end if
        i ← i + 1
        escalonamento(T )
    end while
    
    Algorithm 5 escalonamento
    Require: T , Tanterior, tipo
    if tipo == 1 then
        0.99 · T
    else if tipo == 1 then
        T / 1+0.99·√T
    else T
    1 + Tanterior−T/ ((i−1) / Tanterior ·T ·√T)
    end if

</pre>

## Funções

$$\mathbf{f(x,y) = x^2 + y^2}$$


$$\mathbf{f( x, y) = e^{-(x² + y²)} + 2 \cdot e^{-(x-1.7)^2 + (y - 1.7)^2}}$$


$$ \mathbf{ f(x,y) = -20 \cdot e^{ -0.2 \cdot \sqrt{ -0.5 \cdot (x^{2} + y^{2})} } - e^{0.5 \cdot cos(2 \pi x) + cos(2 \pi y) } + 20 + e^{1}} $$


$$\mathbf{f(x, y) = (x² - 10 \cdot cos(2\pi x) + 10) + (y² - 10 \cdot cos(2 \pi y) +10)}$$


$$\mathbf{f (x, y) = (x - 1)^2 + 100 \cdot (y - x^2)^2}$$


$$\mathbf{f(x,y) = x \cdot sin(4\pi x) - y \cdot sin(4\pi y + \pi) + 1}$$


$$\mathbf{f(x,y) = -sin(x) \cdot sin(x^2/\pi)^{2 \cdot 10} - sin(y) \cdot sin(2y^2/\pi)^{2 \cdot 10}}$$


$$\mathbf{f(x,y) = -(y + 47) \cdot sin(\sqrt{|x/2 + (y + 47)|}) - x \cdot sin(\sqrt{|x - (y + 47)|})} $$

## Caixeiro Viajante

O Algorítimo consiste em minimizar a distancia do trajeto percorrido. Figure 33(b).

<ul>
     <li>Definição de um numero máximo de gerações (iterações) [1000];</li>
     <li>Definição de um numero máximo de população [100] ;</li>
     <li>Possibilidade de aplicar uma função para progredir a população, uma das configurações testadas, Adão e Eva onde a progressão seria $x^2$, sempre o dobro da quantidade de gerações;</li>
     <li>Inicializa um população [100] [50 pontos]. Figure 33 (a);</li>
     <li>Teste de aptidão em modo torneio, onde os melhores são sempre os de menor distancia;</li>
     <li>Geração de uma nova solicitação;</li>
     <li>Durante a geração aplica os métodos de geração cromossômica em aleatórios, elitismo ou cruzamento (pai X mãe = 2 filhos);</li>
     <li>Cruzamentos são realizados sempre que podem;</li>
     <li>Durante o cruzamento são feitos sequenciamentos aleatórios, com probabilidade de 1\% de mutação;</li>
     <li>Repete o processo até acabar as gerações;</li>
</ul>

## 8 Rainhas

O Algorítimo consiste em minimizar a quantidade de ataques ou zera-los. Figure 34 (b).

<ul>
     <li>Definição de um numero máximo de gerações (iterações) [1000];</li>
     <li>Definição de um numero máximo de população [100];</li>
     <li>Possibilidade de aplicar uma função para progredir a população, uma das configurações testadas;</li>
     <li>Inicializa um população [100];</li>
     <li>Teste de aptidão em modo seleção, onde os melhores são as que tem menos probabilidade de se atacar;</li>
     <li>Geração de uma nova solicitação;</li>
     <li>Durante a geração aplica os métodos de geração cromossômica em aleatórios, elitismo ou cruzamento (pai X mãe = 2 filhos);</li>
     <li>Cruzamentos podem ser feitos a uma probabilidade de $75\% < p < 85\%$</li>
     <li>Durante o cruzamento são feitos sequenciamentos aleatórios, com probabilidade de 1\% de mutação;</li>
     <li>Repete o processo até acabar as gerações;</li>
<ul>
