---
layout: post
title: "Python: Por Onde Começo?"
modified:
excerpt: Um rápido passo-a-passo sobre como instalar o Python no seu sistema Linux, Max OSX ou Windows.
categories: programming
tags: [python, install, get started, instalação, programming, programação]
image:
  thumb: python-thumb.png
comments: true
date: 2015-03-21T10:00:17-03:00
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

**Pronto, o Python 3 já está pronto para usar no seu Mac!** Navegue até Aplicações > Utilitários e execute o Terminal. Na tela do terminal, execute o comando `python3` que levará você ao modo interativo do Python, de onde vocẽ já poderá executar seus comandos. Você verá algo semelhante a isto:

{% highlight console %}
$ python3
Python 3.4.1 (default, Apr 11 2014, 13:05:11)
[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
{% endhighlight %}

Para sair do modo interativo e retornar ao terminal, basta executar a função `quit()`.

### Windows

O windows não vem com o Python instalado de fábrica, então para aqueles que utilizam o sistema do tio Gates (a maioria) será preciso instalar tal ferramenta. Siga em frente e baixe o instalador da versão mais atual:

<p style="margin-top: 0px; text-indent: 0; text-align: center; text-align: -moz-center;">
<a markdown="0" href="https://www.python.org/downloads/" class="btn">Baixe o Python 3.x para Windows</a>
</p>

**Obs:** *Escolha o instalador apropriado para a arquitetura do seu Windows: x86 (32 bits) ou x86-64 (64 bits)*.

Duplo clique no instalador baixado para iniciar a instalação. Siga as instruções e aguarde a finalização do processo de instalação. **Pronto, seu Windows já tem o Python instalado!** *Importante*: se vocẽ estiver instalando a versão 2.x do Python, é bem provável que você precise configurar as variáveis de ambiente. No caso da versão 3.x, o instalador já realiza esta etapa automaticamente. Uma vez instalado, você já pode se divertir programando em Python. Basta executar o prompt de comando e entrar no modo interativo.

{% highlight console %}
C:\Users\Gabriel Araujo> python
Python 3.4.2 (v3.4.2:ab2c023a9432, Apr 11 2014, 13:05:11) [MSC v.1600 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
{% endhighlight %}



## Use o modo interativo!

> **Dica:** principalmente para quem está começando a programar, o modo interativo do python (ou shell) é muito importante. Com ele você pode executar comando a comando e assim ter o *feedback* da execução de forma imediata.

O modo interativo é útil, por exemplo, para você fazer "testes rápidos" com alguns comandos --- sabe aquele momento que você não lembra de uma sintaxe ou não sabe se ela vai realmente funcionar? Então, executa no modo interativo apenas este pedaço de código e você tem uma resposta imediata. Como no exemplo descrito abaixo:

{% highlight pycon %}
>>> print 'Olá, mundo!'
  File "<stdin>", line 1
    print 'Olá, mundo!'
                      ^
SyntaxError: invalid syntax
>>> print('Olá, mundo!')
Olá, mundo!
>>>
{% endhighlight %}

O código acima demonstra uma das diferenças entre o Python 2 e 3, em que a palavra reservada `print` deu lugar a função *built-in* `print()`.
