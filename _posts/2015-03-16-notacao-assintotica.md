---
layout: post
title: "Notação Assintótica [Portuguese]"
modified: 2015-03-17T12:01:52-03:00
categories: algorithm-analysis
excerpt: Notação assintótica é uma notação matemática utilizada na análise e comparação de funções f(x) quando x tende à valores grandes (eventualmente ao infinito). Também é um tipo de notação bastante utilizada na análise de complexidade dos algoritmos.
tags: [algorithm analysis, asymptotic notation, big-O]
comments: true
image:
  thumb: http://www.cs.uml.edu/~jannunzi/91.404/classNotes/ch2/images/fig2.1.gif
date: 2015-03-16T01:21:52-03:00
---

{% include _toc.html %}

Na análise de algoritmos é comum definirmos o **tempo de execução** de um algoritmo sob uma entrada específica como sendo o número de "*passos*" executados. A noção abstrata de um passo de execução é conveniente para que o tempo de execução de um algoritmo seja independente de máquina. Assumimos que uma quantidade de tempo constante é requerida para executar cada linha do pseudocódigo do algoritmo. Assim, a execução de cada linha $$i$$ leva o tempo $$t$$, constante.

Apesar de independente de máquina, podemos fazer afirmações concretas sobre o tempo de execução de um algoritmo: "*Sobre qualquer entrada de tamanho $$n$$, o algoritmo $$\mathbf{A}$$ executa com no máximo $$1.62n^2 + 3.5n + 8$$ passos.*"

Entretanto, essa abordagem não é prática por várias razões, incluindo ser trabalhosa e detalhada demais. Além disso, um dos principais objetivos da análise de algoritmos é identificar  classes de algoritmos com comportamentos similares, e para isso nossa descrição precisa ter um nível a mais de granularidade --- o que eu quero dizer com isso é que nossa descrição precisa ser mais genérica, para que as similaridades de algoritmos diferentes sejam aparentes.

Um dos comportamentos que estamos interessados é a taxa de crescimento das várias funções do algoritmo sobre o tamanho da entrada, por exemplo, o tempo de execução -- em outras palavras, o quão rápido o tempo de execução cresce com o tamanho da entrada. E uma maneira genérica de avaliar tal comportamento é por meio da **análise assintótica** dessas funções, qual é insensível a fatores constantes ou termos de baixa ordem. Ou seja, se um determinado algoritmo tem um tempo de execução $$1.62n^2 + 3.5n + 8$$, o que nos interessa saber é que a sua taxa de crescimento é $$n^2$$, ou quadrática.

### Limites Assintóticos Superiores -- $$\mathbf{O}$$

Para uma dada função $$g(n)$$, denotamos por $$O(g(n))$$ (conhecido como notação ***Big-O*** e pronunciado "big-oh de $$g$$ de $$n$$" ou simplesmente "oh de $$g$$ de $$n$$") o conjunto de funções

$$
\begin{align*}
O(g(n)) = \{ f(n) : &\text{ existem constantes positivas } c \text{ e } n_0 \text{ tal que }\\
                    &0 \leq f(n) \leq c \cdot g(n) \text{ para todos } n \geq n_0 \}
\end{align*}
$$

Em outras palavras, uma função $$f(n)$$ pertence ao conjunto $$O(g(n))$$ se existe uma constante positiva $$c$$ tal que $$c \cdot g(n)$$ é um limite superior de $$f(n)$$ para valores de $$n$$ suficientemente grandes, ou seja, $$g(n)$$ é um limite superior assintótico de $$f(n)$$ --- o mais correto seria escrevermos $$f(n) \in O(g(n))$$, mas também é comum escrevermos $$f(n) = O(g(n))$$ para denotar o mesmo.

### Limites Assintóticos Inferiores -- $$\mathbf{\Omega}$$

A notação $$\mathbf{\Omega}$$(.) funciona da mesma maneira que a notação $$O$$(.), exceto que esta descreve o limite assintótico *inferior* da função. Então, formalmente, para uma dada função $$g(n)$$ denotamos por $$\Omega(g(n))$$ (pronunciado "big-omega de $$g$$ de $$n$$" ou simplesmente "omega de $$g$$ de $$n$$") o conjunto de funções

$$
\begin{align*}
\Omega(g(n)) = \{ f(n) : &\text{ existem constantes positivas } c \text{ e } n_0 \text{ tal que }\\
                    &0 \leq c \cdot g(n) \leq f(n) \text{ para todos } n \geq n_0 \}
\end{align*}
$$

Da maneira análoga ao limite superior, dizemos que existe uma constante positiva $$c$$ tal que $$c \cdot g(n)$$ é um limite assintótico inferior de $$f(n)$$ para valores de $$n$$ suficientemente grandes. Em outras palavras, para valores grandes de $$n$$ a função $$f(n)$$ é *pelo menos* $$g(n)$$.

### Limites Assintóticos Restritos -- $$\mathbf{\Theta}$$

Quando um função $$f(n)$$ é ao mesmo tempo $$O(g(n))$$ e $$\Omega(g(n))$$, então dizemos que $$f(n)$$ é $$\Theta(g(n))$$, denotando que $$g(n)$$ é um limite assintótico *retrito*. Na prática, queremos dizer que a função $$f(n)$$ cresce exatamente como $$g(n)$$ dentro de um fator constante. Similarmente, $$\Theta(g(n))$$ é o conjunto de funções

$$
\begin{align*}
\Omega(g(n)) = \{ f(n) : &\text{ existem constantes positivas } c_1 \text{, } c_2 \text{ e } n_0 \text{ tal que }\\
                    &0 \leq c_1 \cdot g(n) \leq f(n) \leq c_2 \cdot g(n) \text{ para todos } n \geq n_0 \}
\end{align*}
$$

Gráficamente podemos ver o efeito desse limites assintóticos na imagem abaixo:

<figure>
	<a href="http://www.cs.uml.edu/~jannunzi/91.404/classNotes/ch2/images/fig2.1.gif"><img src="http://www.cs.uml.edu/~jannunzi/91.404/classNotes/ch2/images/fig2.1.gif"></a>
	<figcaption><a href="http://www.cs.uml.edu/~jannunzi/91.404/classNotes/ch2/2.1%20Asymptotic%20Notation.html" title="http://www.cs.uml.edu/~jannunzi/91.404/classNotes/ch2/2.1%20Asymptotic%20Notation.html">Exemplo de funções com limites assintóticos restritos, superiores e inferiores. (a) restringe uma função dentro de fatores constantes. (b) limita superiormente uma função dentro de fatores constantes. (c) limita inferiormente uma função dentro de fatores constantes</a>.</figcaption>
</figure>

### Limites Assintóticos e Algoritmos

Em particular aos algoritmos, a notação *Big-O* é muito utilizada para descrever os limites assintóticos superiores das funções do tempo de execução e espaço em memória utilizado, chamados de **complexidade de tempo e espaço**, respectivamente. Tais complexidades são comumente descritas para cenários específicos, como o melhor caso, pior caso, e o caso médio.

O termo **melhor caso** se refere ao comportamento do algoritmo sob condições ótimas. Por exemplo: para um algoritmo de ordenação, a condição ótima seria um array de entrada já ordenado. De maneira análoga, o termo **pior caso** se refere as condições extremas de execução do algoritmo, que no exemplo anterior poderia ser um array em ordem decrescente. Já para o **caso médio**, como o próprio nome indica, trivialmente descrevemos uma média da função analisada sob todos os possíveis cenários.

O algoritmo de ordenação ***Insertion sort***, ou *ordenação por inserção*, tem um tempo de execução no pior caso $O(n^2)$, ou seja, no pior cenário possível o tempo de execução do algoritmo será uma função $an^2 + bn + c$, sendo $n$ o tamanho do array de entrada. Essas análises podem ser utilizadas na comparação de performance dos algoritmos, ou até para escolhermos aquele que mais se adequa a nossa situação. Uma ótima referência é o site [**Big-O Cheat Sheet**][bigosheet], que traz as complexidades dos algoritmos e estruturas de dados mais comuns descritos com a notação *Big-O*.

Em outro artigo, falaremos um pouco mais sobre as complexidades de tempo e espaço.

### Leituras adicionais

- [***Big-O Cheat Sheet*** (http://bigocheatsheet.com/)][bigosheet]
- [***Algorithm Design*** by Jon Kleinberg, Éva Tardos][algorithm-design]
- [***Introduction to Algorithms*** by Thomas H. Cormen et. al.][intro-algorithm]

[bigosheet]: http://bigocheatsheet.com/ "Big-O Cheat Sheet"
[intro-algorithm]: http://books.google.com.br/books?id=0BoNBQAAQBAJ "Introduction to Algorithms by Thomas H. Cormen et. al."
[algorithm-design]: https://books.google.com.br/books?id=QWIrAAAAQBAJ "Algorithm Design by Jon Kleinberg, Éva Tardos"
