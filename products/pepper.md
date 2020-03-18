---
layout: product-page
section_id: products
hero-image: pepper_hero2.png
title: PEPPER, a DIY synth kit
sub-title: PEPPER is a DIY kit for experimenting with Bela and your modular synth.
permalink: /products/pepper
---

After the successful launch of <a href="{{ site.url }}/products/salt }}">SALT and SALT+</a>, we heard from a number of hardware enthusiasts who wanted to make their own Bela-powered programmable synth module. In response, we created PEPPER, a DIY kit that includes a custom-designed, bare PCB and a black and silver faceplate.

{% include photocaption.html src='../images/products/pepper/pepper2.png' %}

<h2>A kit for hardware enthusiasts</h2>

PEPPER is a DIY kit for people who love modular synths, Bela, and hardware. PEPPER consists of a bare PCB and a faceplate, and comes with a list of common parts to source. Once you have your parts assembled, follow the <a href="https://github.com/BelaPlatform/bela-pepper/wiki/Building-the-Module">in-depth build guide</a> on the PEPPER Wiki to put it together, attach your Bela unit and the included faceplate, and it's ready to put into your rack.

The parts needed to build PEPPER are common through-hole components, such as resisitors, audio jacks, potentiometers (<a href="https://github.com/BelaPlatform/bela-pepper/wiki/Bill-of-Materials">details of the bill of materials can be found here</a>.) The reason that we chose not to supply the parts is that hardware enthusiasts who like to solder things together likely have some of them already, and we believe in making use of what we already have. 

After soldering PEPPER together, attach your Bela unit (sold separately), and start prototyping straight away.

<h2>Hardware details</h2>

Once assembled, PEPPER is 18HP wide and adds the following to your modular setup:

<h4>I/O (3.5mm / 1/8" jacks):</h4>

- 2 audio in (AC-coupled, 10V pk-to-pk, 44.1kHz, 16bit)
- 2 audio out (DC-coupled, 1.8V pk-to-pk, 0.4V offset, 44.1kHz, 16bit)
- 8 CV in (with pots attenuating, 16bit, 10V safe). Optionally, up to 4x of the CV in sockets can be swapped for trigger ins, leaving the pots connected directly to Bela's analog inputs.
- 8 CV out (16bit, 0-5V)

<h4>Interface:</h4>

- 8 pots (attenuation of CV in)
- 2 buttons
- 10-LED output

<h2>Start experimenting!</h2>

Because it's Bela-powered, PEPPER patches can be programmed using Bela's browser-based IDE. You can program Bela using C++, Pure Data, Supercollider, Csound, and more. Start from scratch, or start from one of the SALT patches that comes pre-loaded in the Bela IDE.

<h2>Things to know:</h2>

PEPPER is a great way to learn to solder or to get some practice! Because it uses through-hole components, the level of soldering skill required is beginner to intermediate.

PEPPER is designed to be attached to a Bela unit, which is sold separately. Because PEPPER relies on analog inputs as well as analog outputs, it requires Bela and is not compatible with Bela Mini.

<p style="text-align: center"><a class='button buy' href="#">GET PEPPER NOW <i class='fas fa-arrow-right'></i></a></p>