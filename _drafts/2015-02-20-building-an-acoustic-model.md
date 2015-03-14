---
layout: post
title: "Building an Acoustic Model (Pt-Br) for CMU Sphinx"
modified:
categories: speech-recognition sphinx
excerpt: How you can build a Brazilian Portuguese Acoustic Model to work with CMU Sphinx.
tags: [speech recognition, cmu sphinx, voxforge, acoustic model ]
image:
  feature:
date: 2015-02-20T19:14:17-03:00
comments: true
---

Have you gone with trouble to build your own acoustic model for [CMU Sphinx](http://cmusphinx.sourceforge.net/)? --- *specially when it needs to support Brazilian Portuguese*, because we know how painful is the lack of audio resources for this particular language --- I will show you how to build a Brazilian Portuguese acoustic model for CMU Sphinx solely using the Voxforge audio resources collection.

First of all, an acoustic model is a statistical model, which means that we need data samples to fit it. These data are simply *transcribed speech audio* --- just an audio file and a respective text file, which has the transcribed speech of the audio as content. --- A collection of this data is frequently called a *speech corpus*.

So, what now? Do I need to build an speech corpus first?

And that's when the Voxforge comes in. [*Voxforge*](http://www.voxforge.org/) is a free collection of transcribed speech for use with Free and Open Source Speech Recognition Engines.
