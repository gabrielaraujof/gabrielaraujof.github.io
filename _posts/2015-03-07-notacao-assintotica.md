---
layout: post
title: "Notação Assintótica [Portuguese]"
modified:
categories: algorithm-analysis
excerpt: Medindo a complexidade dos algoritmos.
tags: [algorithm analysis, asymptotic notation, big-O]
comments: true
image:
  feature:
date: 2015-03-07T01:21:52-03:00
---

Na análise de algoritmos é comum definirmos o **tempo de execução** de um algoritmo sob uma entrada específica como sendo o número de "*passos*" executados. A noção abstrata de um passo de execução é conveniente para que o tempo de execução de um algoritmo seja independente de máquina. Assumimos que uma quantidade de tempo constante é requerida para executar cada linha do pseudocódigo do algoritmo. Assim, a execução de cada linha $$i$$ leva o tempo $$c$$, constante.

Apesar de independente de máquina, podemos fazer afirmações concretas sobre o tempo de execução de um algoritmo:

"*Sobre qualquer entrada de tamanho $$n$$, o algoritmo $$A$$ executa com no máximo $$1.62n^2 + 3.5n + 8$$ passos.*"

Entretanto, essa abordagem não é prática por várias razões, incluindo ser trabalhosa e detalhada demais. Além disso, um dos principais objetivos da análise de algoritmos é identificar  classes de algoritmos com comportamentos similares, e para isso nossa descrição precisa ter um nível a mais de granularidade --- o que eu quero dizer com isso é que nossa descrição precisa ser mais genérica, para que as similaridades de algoritmos diferentes sejam aparentes.

Um dos comportamentos que estamos interessados é a taxa de crescimento das várias funções do algoritmo sobre o tamanho da entrada, por exemplo, o tempo de execução -- em outras palavras, o quão rápido o tempo de execução cresce com o tamanho da entrada. E uma maneira genérica de avaliar tal comportamento é por meio da **análise assintótica** dessas funções, qual é insensível a fatores constantes ou termos de baixa ordem. Ou seja, se um determinado algoritmo tem um tempo de execução $$1.62n^2 + 3.5n + 8$$, o que nos interessa saber é que a sua taxa de crescimento é $$n^2$$, ou quadrática.





- [***Algorithm Design*** by Jon Kleinberg, Éva Tardos][algorithm-design]
- [***Introduction to Algorithms*** by Thomas H. Cormen et. al.][intro-algorithm]

[intro-algorithm]: http://books.google.com.br/books?id=0BoNBQAAQBAJ "Introduction to Algorithms by Thomas H. Cormen et. al."
[algorithm-design]: https://books.google.com.br/books?id=QWIrAAAAQBAJ "Algorithm Design by Jon Kleinberg, Éva Tardos"
