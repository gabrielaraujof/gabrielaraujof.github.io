---
layout: post
title: "Python: Por Onde Começo?"
excerpt: Passo-a-passo de como configurar seu ambiente de desenvolvimento e começar a programar em Python.
categories: programming
tags: [python, intall, get started, instalação, programming, programação]
image:
  thumb: python-thumb.png
comments: true
---

{% include _toc.html %}

**Porque você deveria aprender Python?** A resposta é relativamente simples, como foi detalhado [num artigo da readwrite](http://readwrite.com/2014/07/08/what-makes-python-easy-to-learn). Desde 2008 Python é classificada como uma das oito linguagens de programação mais populares do mundo. Muito disso é devido a ampla adoção do Python por grandes empresas de tecnologia como o Google, Yahoo e NASA. Mas não é só o mercado que indica e impulsiona tal popularidade. Oito das dez melhores faculdades de computação dos Estados Unidos atualmente ensinam Python nas disciplinas de introdução a programação. Isso porque a curva de aprendizado da linguagem é mínima se comparada com a maioria das linguagens.

Além disso, temos uma outra razão --- e talvez a mais importante: *a configuração necessária para você começar a programar em Python em qualquer computador é **muito** simples*. Então chega de blábláblá e vamos ao que interessa!


<figure>
	<img src="/images/python-logo.png">
	<figcaption><a href="https://www.python.org/community/logos/" title="Python logo at www.python.org">www.python.org</a></figcaption>
</figure>

## Instalando o Python

### Linux

A maioria dos sistemas GNU/Linux já vem com o Python pré-instalado, então você não tem absolutamente **nada a fazer** neste quesito --- que maravilha! Entretando, algumas distros trazem apenas a versão 2.x do Python. Se você prefere a versão 3.x você precisará instalá-la, mas isto é bastante simples. (*Eu fortemente recomendo utilizar a versão 3. Vários recursos úteis da linguagem não estão disponíveis nas versões anteriores*.)

> Estou usando como referência o Ubuntu/LinuxMint/Debian. Para outras distribuições você precisará compilar o Python antes de instalá-lo. Abordarei este caso num outro post em breve.

Abra o terminal e execute o seguinte comando:

{% highlight console %}
$ sudo apt-get update
$ sudo apt-get install python3
{% endhighlight %}

**Pronto, você já tem o Python 3 instalado e pronto para usar!** No mesmo terminal execute o comando `python3` e você entrará no modo interativo do Python. Você verá algo como:

{% highlight console %}
$ python3
Python 3.4.0 (default, Apr 11 2014, 13:05:11)
[GCC 4.8.2] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
{% endhighlight %}

A partir daí você já pode executar seus comandos em Python. Para sair do modo interativo, basta executar `quit()`.

### Mac OSX

Assim como os sistemas GNU/Linux, a versão 2.x do Python já vem pré-instalada no Mac OSX. Se você for utilizar a versão 3.x, precisaremos instalá-la. Baixe a versão mais atual do Python:

<p style="margin-top: 0px; text-indent: 0; text-align: center; text-align: -moz-center;">
<a markdown="0" href="https://www.python.org/downloads/" class="btn">Baixe o Python 3.x para Mac OSX</a>
</p>

Em seguida, duplo clique no arquivo **.pkg** baixado para iniciar a instalação (*é possível que você precise informar seu usuário e senha de administrador*). Siga as instruções na tela que aparece, aceite os termos de licença e confirme a instalação.

**Pronto, o Python 3 já está pronto para usar no seu Mac!** Navegue até Aplicações > Utilitários e execute o Terminal. Na tela do terminal, execute o comando `python3` que levará você ao modo interativo do Python, de onde vocẽ já poderá executar seus comandos Python. Você verá algo semelhante a isto:

{% highlight console %}
$ python3
Python 3.4.1 (default, Apr 11 2014, 13:05:11)
[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
{% endhighlight %}

Para sair do modo interativo e retornar ao terminal, basta executar a função `quit()`.

### Windows

O windows não vem com o Python instalado de fábrica, então para aqueles que utilizam o sistema do tio Gates (a maioria) será preciso instalar a versão mais atual do Python. Siga em frente e baixe o instalador no site oficial do Python:

<p style="margin-top: 0px; text-indent: 0; text-align: center; text-align: -moz-center;">
<a markdown="0" href="https://www.python.org/downloads/" class="btn">Baixe o Python 3.x para Windows</a>
</p>

**Obs:** *Escolha o instalador apropriado para a arquitetura do seu Windows: x86 (32 bits) ou x86-64 (64 bits)*.

Duplo clique no instalador baixado para iniciar a instalação. Siga as instruções e aguarde a finalização do processo de instalação.

Por padrão, o Python não configura a variável de ambiente **PATH** para que seja possível você ter o controle sobre qual instalação do Python será configurada como padrão --- dessa forma você pode ter o Python 2 e 3 instalados no mesmo sistema, bastando configurar a variável de ambiente para alternar entre os dois.

Para configurar a variável de ambiente, basta adicionar os diretórios de instalação do Python para a variável **PATH**. Por exemplo, se você instalou o Python no diretório padrão `C:\Python34\`, basta adicionar para a variável **PATH**:

{% highlight text %}
C:\Python34\;C:\Python34\Scripts\
{% endhighlight %}

Depois de configurado, ...


## Seu primeiro programa

{% highlight py3 pycon linenos %}
>>> nome = input('Seu nome: ')
Seu nome: gabriel
>>> print( 'Olá', nome )
Olá gabriel
>>>
{% endhighlight %}

## Configurações adicionais
