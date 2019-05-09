---
layout: faq
section_id: faq
title: Frequently Asked Questions
---

## Your Bela queries answered

Welcome to the Frequently Asked Questions page! Please browse the questions and answers below. If your query isn't answered here, please email us.

1. <a href="#1" class="page-scroll">Is the number of analog inputs (or outputs) extendable?</a>
2. <a href="#2" class="page-scroll">Can I connect a microphone to the audio input?</a>
3. <a href="#3" class="page-scroll">So you are running Pd and and you claim less than one millisecond latency? How is that possible, given Pd's minimum buffer size is 64 samples?</a>
4. <a href="#4" class="page-scroll">Is it the same as an Arduino with an MP3 shield?</a>
5. <a href="#5" class="page-scroll">Can you make a VST plugin that talks to Bela?</a>
6. <a href="#6" class="page-scroll">Can the audio hardware be accessed via normal audio drivers or Jack?</a>
7. <a href="#7" class="page-scroll">How does Bela compare to Axoloti?</a>
8. <a href="#8" class="page-scroll">How does it compare to the Raspberry Pi 2 with a USB dongle?</a>
9. <a href="#9" class="page-scroll">Will you offer an enclosure?</a>
10. <a href="#10" class="page-scroll">What about customs duties?</a>
11. <a href="#11" class="page-scroll">Why not use a specialised DSP processor instead of the ARM CPU?</a>
12. <a href="#12" class="page-scroll">Can I connect Bela to my Arduino?</a>
13. <a href="#13" class="page-scroll">Does it play uncompressed audio files from an SD Card? Will it support MP3?</a>
14. <a href="#14" class="page-scroll">Can it do convolution reverb?</a>
15. <a href="#15" class="page-scroll">What kind of Pd does it use?</a>
16. <a href="#16" class="page-scroll">What Linux distribution are you running?</a>
17. <a href="#17" class="page-scroll">What voltage levels are supported?</a>
18. <a href="#18" class="page-scroll">Are there any I2S or SPI buses available on board?</a>
19. <a href="#19" class="page-scroll">What BBB header pins are used by the Bela cape?</a>
20. <a href="#20" class="page-scroll">Can I run [audio program X] on Bela?</a>

### <a id="1"></a>Is the number of analog inputs (or outputs) extendable?

You can have more inputs with a lower sampling rate using external multiplexers. We experimented with up to 32 inputs at 5 kHz, but you can probably reach 128 inputs at 1.25kHz without problems. Multiplexing analog output is more complicated as you would probably need a sample-and-hold on each channel, which would be expensive.

### <a id="2"></a>Can I connect a microphone to the audio input?

Yes, the audio codec has an on-board audio preamplifiers which can provide up to 59.5dB of gain, adjustable individually for each audio channel. No phantom power or plug-in power are provided, though 5V is available elsewhere on the board to power an electret capsule. The audio codec is a TLV320AIC3104.

### <a id="3"></a>So you are running Pd and and you claim less than one millisecond latency? How is that possible, given Pd's minimum buffer size is 64 samples?

For two reasons. First, we are not running the Pd program itself, and second one, we are not using the Linux ALSA drivers. Pd patches are compiled into C code using the Heavy Audio Tools. The C code produced is highly optimised and is automatically wrapped into our C++ API. This bypasses the whole Linux kernel (and ALSA) and allows it to run with buffer sizes as small as 2 audio samples, giving a rountrip latency below 1ms for audio (because the ADC/DAC have some built-in latency) and below 100us for analog (whose converters are faster).

### <a id="4"></a>Is it the same as an Arduino with an MP3 shield?

Bela has far more computing capability and speed than an arduino, including the ability to run Linux and do complex DSP calculations in real time.

### <a id="5"></a>Can you make a VST plugin that talks to Bela?

You can access Bela through standard ethernet protocols so, for instance, communication using OSC is quite easy.

### <a id="6"></a>Can the audio hardware be accessed via normal audio drivers or Jack?

Not at the moment, though this might be possible in future.

### <a id="7"></a>How does Bela compare to Axoloti?

Axoloti is a bare-metal microcontroller board with an 168MHz ARM Cortex-M4 microcontroller on it. Bela is a computer with a 1GHz ARM Cortex-A8 CPU which has much more processing power and built-in vector floating point support. Bela runs on Linux and, as such, gets all the extra functionalities that come with it (storage, network, USB, onboard compiling). Bela also takes advantage of a more powerful CPU and the two onboard 200MHz Programmable Realtime Units.

At the same time, Bela runs ON TOP of Linux (that is: at a higher priority), so that the audio performance are never interrupted by what else is happening on the board: you get the best of Linux without the performance overhead.

Bela has 16-bit analog inputs and outputs (8 each) sampled at 22.05kHz which can conveniently double up as audio inputs, Axoloti has 15 channels of 12-bit analog inputs sampled at 3kHz, two of those channels can also switch to 12-bit analog outputs. Bela also has two onboard speaker amplifiers. On the other hand, Axoloti has built-in 5-pin MIDI jacks which Bela does not have, though both can use MIDI over USB. Axoloti has its own graphical development environment, which allows you to integrate C++ snippets, whereas for Bela you can either compile Pd patches using the Heavy Audio Tools or write plain C++ code.

### <a id="8"></a>How does it compare to the Raspberry Pi 2 with a USB dongle?

With a 4-core CPU, the Pi 2 has more raw processing power than the BeagleBone Black, but it still cannot match the low-latency performance of Bela because it is reliant on the standard Linux audio drivers. Latency on the Raspberry Pi depends on the particular USB audio device and the software environment, but latencies of 20ms or higher are common (9ms is the best measurement we have seen under ideal conditions). Compare this to 1ms or less for Bela. Additionally, Bela comes with 16-bit analog I/O and plenty of digital I/Os, all sampled at audio rate, which is not possible on the Pi.

### <a id="9"></a>Will you offer an enclosure?

Not at the moment. Bela is meant to be embedded inside your project, so we expect an enclosure will not be needed in most cases. You can go for aftermarket plastic, wood or metal enclosures.

### <a id="10"></a>What about customs duties?

Items are shipped from the United Kingdom. Except for shipping, the price is the same anywhere in the world. You are responsible for any taxes or duties upon arrival in your country.

### <a id="11"></a>Why not use a specialised DSP processor instead of the ARM CPU?

DSPs are typically designed to do efficient audio computations, not to run multifunction operating systems like Linux. There are plenty of good DSP development boards out there which offer high-performance audio, but they lack the flexibility of Bela, and most of them do not have the same degree of analog and digital I/O either. DSP development boards also tend to be expensive. Finally, the gap between DSPs and general-purpose CPUs has been closing in recent years thanks to features like the NEON vector floating point instruction set on the ARM Cortex-A series.

### <a id="12"></a>Can I connect Bela to my Arduino?

Yes, via USB, I2C, UART, or other protocols. But we encourage you to use the analog and digital I/Os built in to the Bela cape!

### <a id="13"></a>Does Bela play uncompressed audio files from an SD card? Will it support MP3?

Yes. You can use any library in Linux that supports these. libsoundfile is already bundled with the SD card image.

### <a id="14"></a>Can it do convolution reverb?

A few years ago a student in our lab implemented a convolution reverb on a standard, unoptimized Beaglebone Black, with impulse responses as long as 12 seconds. So yes, the processing power is there.

### <a id="15"></a>What kind of Pd does it use?

Pd-vanilla patches are compiled using Heavy, a product of Enzien Audio. Please refer to Enzien Audio for Pd and Heavy questions: https://enzienaudio.com/ List of Pd objects: https://enzienaudio.com/docs/pdobjects.html

### <a id="16"></a>Which Linux distribution are you running?

We are running a modified Debian distribution with additional drivers and scripts for running the Bela code and IDE.

### <a id="17"></a>Which voltage levels are supported?

Audio I/O levels depend on the adjustable settings of the audio codec. You can comfortably plug in a guitar, a dynamic microphone, a piezo pickup, most stuff really, having up to 59.5dB of gain at your disposal. You can refer to the TLV320AIC3104 datasheet for more details.

Analog ins are in the range 0-4.096V (inputs are 5V tolerant); Analog outs are in the range 0-5V; Digital I/O levels are 0/3.3V. Mind that these are the BeagleBone's AM3358's own digital pins, so make sure you NEVER exceed 3.3V or you will brick your BeagleBone Black.

### <a id="18"></a>Are there any I2S or SPI buses available on board?

The cape uses one shared SPI bus for the DC-coupled ADC and DAC and it uses I2S to communicate with the stereo audio codec. The speed of this currently is the main limiting factor of the sampling rate of the analog channels. Although there is one extra SPI peripheral on the AM3358 chip, it uses the same pins as the I2S bus so they cannot be used simultaneously.

### <a id="19"></a>What BBB header pins are used by the Bela cape?

The Bela cape uses pin 24 on header P8 and pins 10-15-17-18-19-20-21-22-23-24-25-26-28-29-30-31 on header P9. Additionally, 16 of the remaining pins can optionally be used for Digital I/O, as you can see from the Pin Diagram.

### <a id="20"></a>Can I run [audio program X] on Bela?

Bela does not use the regular Linux ALSA audio drivers, so your software needs to explicitly support Bela. At the moment our C/C++ API and the Pd workflow provided through Heavy are the only supported way of developing for Bela, though we are actively working on support for other audio programs (to be announced). If you have access to the source code for your audio program, you may be able to edit it to run on Bela. On the other hand, most generic C/C++ libraries are likely to work fine within a Bela program.
