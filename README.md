Origami: the synth that breaks the rules (or not?)
![Logo Origami](https://github.com/user-attachments/assets/805f6224-f6e8-4783-ae50-3f2e9cf1f2a2)

Origami is a synthesizer capable of generating sounds through Phase Modulation (PM), Frequency Modulation (FM), Amplitude Modulation (AM), Phase Distortion (PD), Wave Folding, and Additive Synthesis. Its intermodularity makes it super fun and intuitive to explore and create complex sounds!

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

![1](https://github.com/user-attachments/assets/809f5ae6-09f3-4d24-bfaa-d2cc60eb9987)

The synth is designed to stay in tune in a wide range of temperatures (16-40°) by using thermistors, cermet trimmers and NP0 capacitors.

![3](https://github.com/user-attachments/assets/0741ba0a-dae5-40de-8d5b-746bfd7262bb)

Code for the MIDI interface:
https://github.com/PaoloEstorm/MIDI-to-CV

PCB Design & Schematics:
https://oshwlab.com/estorm/origami

Thermistor Link (UK)
https://amzn.eu/d/gloktOI

Thermistor Link (IT)
https://amzn.eu/d/2uYDJzZ

AC/DC Adapter Link (UK)
https://amzn.eu/d/dQfOkpd

AC/DC Adapter Link (IT)
https://www.amazon.it/dp/B09MYL5KBQ?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1
