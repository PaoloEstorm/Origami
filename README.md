# Origami: the synth that breaks the rules (or not?)
![Logo Origami](https://github.com/user-attachments/assets/805f6224-f6e8-4783-ae50-3f2e9cf1f2a2)

## Estorm Origami is the first Analog Synthesizer capable of Phase Modulation (PM), Frequency Modulation (FM), Amplitude Modulation (AM), Phase Distortion (PD), Wave Folding, and Additive Synthesis. Its intermodularity makes it fun and intuitive to explore and create complex sounds!

[![This Synth Breaks The Rules](https://github.com/user-attachments/assets/e44ff963-27a0-4a93-9d2d-e1a0a9317ccf)](https://youtu.be/fYJeXG9gMpo "This Synth Breaks The Rules")

The project was born in 2021 from a simple yet ambitious idea: creating a synth that generates complex, metallic, and percussive sounds by bending and distorting waves instead of using classic subtractive synthesis.

I've always been fascinated by FM synthesis and the mystery surrounding it. How does it really work? Why do digital FM synths have such a unique character?

Back then, with my very limited knowledge of the theory behind FM, I started experimenting. But I quickly hit a wall: modulating the frequency of an analog oscillator resulted in a completely inharmonic output. It sounded awful—nowhere near those legendary synths used in the 80s. I tried everything: linear FM, exponential FM… but nothing worked. No difference at all.

So I started wondering: maybe FM synthesis is simply impossible in analog?
Spoiler: NO, it’s not.

After tons of research, I finally figured out the missing piece: what we call "FM synthesis" in digital synths isn't actually Frequency Modulation—it’s Phase Modulation (PM). The two terms get mixed up all the time, but they’re fundamentally different. Sure, in some cases they might produce similar sounds, but they work in totally different ways.

That’s when I took inspiration from an old project by Yusynth called "Saw Animator" and developed a system to modulate phase using a sawtooth pilot signal, without actually changing the oscillator's frequency.

You can get a feel for the concept in this simulation:
Move the PHASE bar and see what happens!

[![Phase Mod Test](https://github.com/user-attachments/assets/c3b8cbf0-812e-426f-aa82-e60d479ab672)](https://tinyurl.com/26c96skb "Phase Mod Test")

After tons of trial and error, I finally designed a simple but effective system that can shift phase up to 1080° (three full 360° rotations). Based on my analysis of various synths, that’s more than enough to create deep modulations and complex timbres.

The synth is designed to stay in tune in a wide range of temperatures (16-40°) by using thermistors, cermet trimmers and NP0 capacitors.

![3](https://github.com/user-attachments/assets/0741ba0a-dae5-40de-8d5b-746bfd7262bb)

Once I fine-tuned the phase modulation oscillator, I implemented waveform converters to generate triangle, sine, and square waves from a sawtooth signal.

![4](https://github.com/user-attachments/assets/5243340a-e377-48f6-9401-48cd9d5810c8)

Origami is made out of two main modules: the Operator module and the PSU module.
Each Operator module comes with an oscillator, a wavefolder, a VCA, and a special envelope generator—I'll tell you all about it below.
In the PSU module, you'll find power delivery circuitry, a MIDI-to-CV converter, a slider that can be used both for calibration and for controlling any parameter, and a mixer.

![IMG_6359](https://github.com/user-attachments/assets/7fb8635e-9763-40ce-b6ee-279a953f4b3e)

Four Operator modules are connected in series with a final PSU module.
I chose this modular system to keep PCB production costs low, but it can easily be adapted into a single PCB design or even expanded with additional future modules to add future functionalities.

![PCB_3D](https://github.com/user-attachments/assets/034dcf1f-b040-475c-9769-999bdc3216ca)

The front panel can be made as a fiberglass PCB or aluminum, directly alongside the PCBs of the modules.

![11](https://github.com/user-attachments/assets/4afcab0b-4374-4592-86e3-4aad3e6e634d)

![IMG_1875](https://github.com/user-attachments/assets/f2063af9-dec1-4855-baaf-c1de14402843)

I built the case using a 4mm MDF sheet, cut and assembled with hot glue. You'll find a schematic in the attachments.

![IMG_1935](https://github.com/user-attachments/assets/d6924d77-4872-414d-8fd6-fa7013fcd34f)

Coming up, I'll be designing a new version of Origami using almost exclusively SMD components. This will significantly reduce both production costs and assembly time.

## If you liked my project, stick around for more! Follow me to stay updated on all my past, present, and future creations!

## PCB Design & Schematics:
## https://oshwlab.com/estorm/origami

## Code for the MIDI interface:
## https://github.com/PaoloEstorm/MIDI-to-CV

PCBs and front panel by JLCPCB

Thermistors
https://amzn.eu/d/2uYDJzZ

AC/DC Adapter
https://www.amazon.it/dp/B09MYL5KBQ?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1

Potentiometers
https://it.rs-online.com/web/p/potenziometri/1670101

Potentiometer Knobs
https://it.aliexpress.com/item/32955417001.html

Precision Trimmer
https://amzn.eu/d/e85j6hm

Resistors, capacitors, trimmers, slide switches, op-amps, diodes, transistors & chip sockets
http://www.graziacomponenti.it/index.php

Pin Headers
https://amzn.eu/d/9up7Byu
https://amzn.eu/d/d3ZOwLH

Audio jacks
https://amzn.eu/d/7R5lwUS

LEDs
https://amzn.eu/d/5YtIw9u
