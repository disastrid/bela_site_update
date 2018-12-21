---
layout: default
hero-image: index.jpg
title: The Bela Story
permalink: /our-story
---

Bela is a project of the [Augmented Instruments Laboratory](http://instrumentslab.org), a research team in the [Centre for Digital Music](http://c4dm.eecs.qmul.ac.uk) at Queen Mary University of London. 

Bela's origins date back to 2014, when we were building a new musical instrument called the [D-Box](https://blog.bela.io/2016/11/28/dbox/), a research project funded by the UK [Engineering and Physical Sciences Research Council](http://epsrc.ac.uk). The D-Box is a hackable musical instrument: while it appears simple at first, the user can rewire its circuits in exploratory ways to create unexpected and glitchy sounds (read more about the D-Box in our papers from [ICLI 2014](https://qmro.qmul.ac.uk/xmlui/bitstream/handle/123456789/7204/MCPHERSONDesignandUse2014.pdf?sequence=2) and [NIME 2015](http://www.nime.org/proceedings/2015/nime2015_258.pdf)).

{% include photocaption.html src="the-story/d-box.jpg" caption="The D-Box hackable musical instrument." %}

The D-Box needed a specialised set of capabilities that we couldn’t find in any existing platform. It had to be fully self-contained, generating audio without a computer. It needed enough processing power to run complex synthesis processes. Beyond audio processing, it needed high-resolution analog inputs and outputs to power the rewirable circuits, and onboard amplifiers to power a speaker. Finally, all of the audio and analog I/O needed to run with extremely low latency. What we couldn’t find, we had to build ourselves. Bela was born.

## From Research Project to Maker Platform

After building the D-Box, we realised that the low-latency embedded platform we had made for it was useful for many of our other research projects. We started teaching a class in real-time digital signal processing in early 2015, which had previously been taught using expensive and unwieldy hardware DSP boards. We kept the hardware that powered the D-Box but replaced its custom code with a simple and open programming interface. With this change, anyone could write code that made use of low-latency audio, analog and digital I/O.

We originally called our platform BeagleRT after the [BeagleBone Black](http://beagleboard.org) single-board computer that it runs on (read more about the first release in [this paper](https://www.eecs.qmul.ac.uk/~andrewm/mcpherson_aes2015.pdf)). Later, we changed the name to the shorter and simpler Bela.

{% include photocaption.html src="the-story/bela-connected.png" %}

The first versions of Bela were programmed in C or C++, and needed a compiler running on the host computer. But in 2015, we moved all the tools needed to build projects onto the board itself and created an easy-to-use IDE that runs in the browser. Around the same time, we added support for the popular [Pure Data](http://puredata.info) (Pd) graphical audio programming language.

All the while, we worked with a gradually growing circle of collaborators to get Bela into circulation at other universities and in the wider community. In turn, the community helped us add features like support for the [SuperCollider](https://supercollider.github.io/) and [FAUST](http://faust.grame.fr) programming languages. By 2016, we were ready for our public launch.

## Growing a Community: Kickstarter and Beyond

On 29 February 2016, we launched the [Bela Kickstarter campaign](https://www.kickstarter.com/projects/423153472/bela-an-embedded-platform-for-low-latency-interact) to fund the first round of Bela boards. We kept our expectations modest, looking to raise £5,000 for a small first run. However, we tripled that goal in the first 24 hours, and the campaign went on to raise more than £50k from over 500 backers. With their support, we not only built and shipped the first large batch of [Bela kits](https://shop.bela.io/bela/starter-kit), but were were also able to create the [Multiplexer](https://shop.bela.io/bela-accessories/bela-mux-capelet) and [Audio Expander](https://shop.bela.io/bela-accessories/bela-audio-expander-capelet) accessories to extend Bela's capabilities even further.

{% include youtube.html id="Os2ljj1cIog" %}

After Kickstarter, we have launched the [Bela shop](https://shop.bela.io) so Bela is available to customers worldwide. We have also created online resources for our growing community, including a support [forum](http://forum.bela.io), a [blog](http://blog.bela.io) featuring projects from the wider Bela community, a technical info [wiki](https://github.com/BelaPlatform/Bela/wiki), and repositories with open-source [hardware](https://github.com/BelaPlatform/bela-hardware) and [software](https://github.com/BelaPlatform/Bela) designs. It has been especially rewarding to see the amazing projects that people are making with Bela, ranging from musical instruments, audio effects, and interactive installations to robotics projects, laboratory experiments, classroom teaching and more. You can read more about our efforts to build a maker community in [this paper](https://qmro.qmul.ac.uk/xmlui/bitstream/handle/123456789/19132/Mcpherson%20Building%20a%20Maker%20Community%202017%20Accepted.pdf?sequence=1), presented at CHI 2017.

{% include youtube.html id="Pp3dPinF6uM" %}

In February 2018 we launched [Bela Mini](https://shop.bela.io/bela-mini), all the most popular Bela features condensed into an even smaller package. Bela Mini has the same ultra-low-latency performance and connectivity for audio, analog and digital signals, but at one-third the size of Bela Original it fits in more places than ever before.


