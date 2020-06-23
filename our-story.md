---
layout: default
hero-image: index.jpg
title: The Bela Story
permalink: /our-story
---

Bela is a project of the [Augmented Instruments Laboratory](http://instrumentslab.org), a research team in the [Centre for Digital Music](http://c4dm.eecs.qmul.ac.uk) at Queen Mary University of London. 

Bela was created in 2014, when we were building a new musical instrument called the [D-Box](https://blog.bela.io/2016/11/28/dbox/), a research project funded by the UK [Engineering and Physical Sciences Research Council](http://epsrc.ac.uk). The D-Box is a hackable musical instrument that allows the player to rewire its circuits in exploratory ways to create unexpected sounds (read more about the D-Box in our papers from [ICLI 2014](https://qmro.qmul.ac.uk/xmlui/bitstream/handle/123456789/7204/MCPHERSONDesignandUse2014.pdf?sequence=2) and [NIME 2015](http://www.nime.org/proceedings/2015/nime2015_258.pdf)).

{% include photocaption.html src="the-story/d-box.jpg" caption="The D-Box hackable musical instrument." %}

The D-Box needed a specialised set of capabilities that we couldn’t find in any existing platform. It had to be fully self-contained, generating audio without a computer. It needed enough processing power to run complex synthesis processes. Beyond audio processing, it needed high-resolution analog inputs and outputs to power the rewirable circuits, and onboard amplifiers to power a speaker. Finally, all of the audio and analog I/O needed to run with extremely low latency. What we couldn’t find, we had to build ourselves. Bela was born.

## From Research Project to Maker Platform

We soon realised that the low-latency embedded platform we had made for the D-box had wider applications. The first was teaching; we started teaching a class in real-time digital signal processing in early 2015, which had previously been taught using expensive and unwieldy hardware DSP boards. 

{% include photocaption.html src="the-story/bela-connected.png" %}

This first versions of Bela only supported programming in C/C++ and had a complicated Linux toolchain. We moved all the tools needed to build projects onto the board itself, and created an easy-to-use IDE that runs in a web browser. We also added support for the popular [Pure Data](http://puredata.info) (Pd) graphical audio programming language, so interactive programming didn't only have to be done in C++. (Bela now supports many languages, thanks to community contributions. The Bela community has helped us add features like support for [SuperCollider](https://supercollider.github.io/) and [FAUST](http://faust.grame.fr).)

## Growing a Community: Kickstarter and Beyond

In February 2016 we launched [Bela on Kickstarter](https://www.kickstarter.com/projects/423153472/bela-an-embedded-platform-for-low-latency-interact). This campaign raised more than £50k from over 500 backers, and we were not only able to shop the first Bela systems, but also created Bela's Multiplexer Capelet and Audio Expander.

{% include youtube.html id="Os2ljj1cIog" %}

Bela is now available to customers worldwide through the [Bela shop](https://shop.bela.io). We have also created online resources for our growing community, including a support [forum](http://forum.bela.io), a [blog](http://blog.bela.io) featuring projects from the wider Bela community, a [knowledge base](https://learn.bela.io) for learning how to create with Bela, as well as a huge array of repos on our [Github](https://github.com/belaPlatform).

{% include youtube.html id="Pp3dPinF6uM" %}

## Later additions

In 2018 we added [Bela Mini](https://shop.bela.io/bela-mini) to the Bela product line. Bela Mini has all the most popular Bela features condensed into a tiny package, with all the same performance for sensors and sound.

In 2019 we funded Trill touch sensors on [Kickstarter](https://www.kickstarter.com/projects/423153472/trill-touch-sensing-for-makers?ref=5h34wt&token=6b96b598). Trill is a family of capacitive touch sensors that make it easy to add touch interaction to digital projects. Though created by the Bela team, Trill is compatible not only with Bela but also with maker platforms like Arduino, Teensy, and Raspberry Pi. Read all about Trill at [bela.io/trill](https://bela.io/trill).