---
layout: about
section_id: about
hero-image: hero-1.jpg
title: All about Bela
---

# What is Bela?

Bela is an embedded computing platform for creating beautifully reponsive interactive applications. Bela provides ultra-low latency, high quality audio, analog and digital I/O in a tiny self-contained package that can be easily embedded. Built upon the [BeagleBone](https://beagleboard.org/) family of open-source embedded computers, Bela combines the processing power of an embedded computer with the timing precision and connectivity of a microcontroller.

Bela features an on-board, browser-based IDE, making it easy to get up and running without requiring any additional software. The end result: digital instruments and interactive objects that are faster to develop and more responsive to use.

<span class="list-header">Bela is fast.</span> Bela's dedicated hardware and software environment provides hard real-time performance with 1ms latency while retaining the capabilities and power of a 1GHz embedded computer running Linux.

<span class="list-header">Bela is connected.</span> Use Bela's stereo audio input and output to create musical instruments and audio effects. Connect to the physical world with Bela Original's 8 analog inputs and outputs (or Bela Mini's 8 analog inputs), as well as 16 digital I/O pins. You can also use ethernet, USB (including MIDI) and SD card storage.

<span class="list-header">Bela is small.</span> Bela's compact form factor means that it easily integrates into portable interactive objects, and the condensed Bela Mini means that it fits in more places than ever before. Connect to your computer to program Bela, and then power from an external battery to run in standalone mode - no laptop required.

<span class="list-header">Getting started is easy.</span> Connect Bela by USB, launch the on-board IDE, and start coding right away in C++, PureData, SuperCollider, or FAUST. Our IDE also features everything interactive creators need, like an intuitive interface, a huge library of example projects, and an in-brownser oscilloscope.

# Why latency matters

{% include latency-graph.html %}

# The Hardware

Bela comes in two versions. The original Bela board has 8 channels of 16-bit analog I/O, 16 digital I/O, stereo audio I/O, and on-board speaker amps. We have also developed the tiny Bela Mini, by taking the most popular features of Bela and condensing them into a form factor 1/3 the size.

{% include photocaption.html src='bela_comparison.png' %}

# The Software

Bela runs a custom audio processing environment based on the Xenomai real-time Linux extensions. Your code runs in hard real-time, bypassing the entire operating system to go straight to the hardware. We have written a custom audio driver using the Programmable Realtime Unit (PRU), a microcontroller on the same chip as the CPU. This driver is capable of buffer sizes as small as 2 audio samples for very low latency, and its performance is not affected by other system load. No other embedded Linux platform can match this performance. (Read more in [this publication](http://eecs.qmul.ac.uk/~andrewm/mcpherson_aes2015.pdf), which describes the technical aspects of Bela in detail.)

{% include photocaption.html src='bela_software.png' %}

For development, Bela lets you code the way that suits you best, and gives you the tools you need to do it. Plug in your Bela and launch our in-browser IDE, where you can write code in C++, SuperCollider, FAUST, Csound, upload PureData patches. The IDE also includes an extensive library of example projects, illustrating synthesis, sensor handling, and a range of other techniques in a variety of languages. There is also an in-browser oscilloscope which lets you visualise multiple channels of data simulteanously, without disconnecting the board - an essential tool for sensor debugging. 

# Who makes Bela?

Bela was born in the [Augmented Instruments Laboratory](http://instrumentslab.org/), in the [Centre for Digital Music](http://c4dm.eecs.qmul.ac.uk/) at [Queen Mary University of London](https://www.qmul.ac.uk/). Bela is now developed and produced by Augmented Instruments Ltd in London, UK. Learn more about Bela's origins on the [Our Story](our-story) page.

# Making products with Bela

<p class="list-header">I want to make a commercial product with Bela, how do I make that happen?</p>

The Bela team is always happy to talk to people wanting to integrate Bela into commercial products, and we're available for consultancy to integrate Bela into applications for commercial deployment. Please <a href="mailto:info@bela.io">drop us an email</a> with details of your plan, and we'd be happy to discuss it.

<p class="list-header">I've made something really cool with Bela! Can I put your logo on it?</p>

Bela's name and logo are trademarked and reserved for commercial products that are produced by or licensed by Bela and Augmented Instruments Ltd.

If you've made something with Bela and want to use our logo, we have a logo especially for community products! Download it <a href="bela_community_logo.svg" target="new">here</a>, and feel free to use it on physical products or on a website to advertise something that you've made with Bela. 

<p class="list-header">I've made something really cool with Bela! Can I call what I've made a Bela product?</p>

Calling something a "Bela product" is something reserved only for things made or licensed by Bela and Augmented Instruments Ltd, and should not be used to describe unofficial product variants. But, here's some ways you can integrate Bela with your product name:

- [ProductName] for Bela
- [ProductName] (Bela-compatible)

Names such as "Bela [ProductName]", "[ProductName] Bela", or "Bela-compatible [ProductName]" should be avoided. If you're not sure, please <a href="mailto:info@bela.io">drop us a line</a> and we can advise.