Origami: the synth that breaks the rules (or not?)

Origami is a synthesizer capable of generating sounds through Phase Modulation (PM), Frequency Modulation (FM), Amplitude Modulation (AM), Phase Distortion (PD), Wave Folding, and Additive Synthesis. Its intermodularity makes it super fun and intuitive to explore and create complex sounds!

[![This Synth Breaks The Rules](https://github.com/user-attachments/assets/e44ff963-27a0-4a93-9d2d-e1a0a9317ccf)](https://youtu.be/fYJeXG9gMpo "This Synth Breaks The Rules")

The project was born in 2021 from a simple yet ambitious idea: creating a synth that generates complex, metallic, and percussive sounds by bending and distorting waves instead of using classic subtractive synthesis.

I've always been fascinated by FM synthesis and the mystery surrounding it. How does it really work? Why do digital FM synths have such a unique character?

Back then, with my very limited knowledge of the theory behind FM, I started experimenting. But I quickly hit a wall: modulating the frequency of an analog oscillator resulted in a completely inharmonic output. It sounded awful—nowhere near those legendary synths used in the 80s. I tried everything: linear FM, exponential FM… but nothing worked. No difference at all.

So I started wondering: maybe FM synthesis is simply impossible in analog?
Spoiler: NO, it’s not.

After tons of research, I finally figured out the missing piece: what we call "FM synthesis" in digital synths isn't actually Frequency Modulation—it’s Phase Modulation (PM). The two terms get mixed up all the time, but they’re fundamentally different. Sure, in some cases they might produce similar sounds, but they work in totally different ways.

That’s when I took inspiration from an old project by Yusynth—the legendary "Saw Animator"—and developed a system to modulate phase using a sawtooth pilot signal, without actually changing the oscillator's frequency.

You can get a feel for the concept in this simulation:
Move the PHASE bar and see what happens!

https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEDoBYEE4AcYFwMz5iqoBMqykylyApgLRhgBQAhiPpBWAGxX5ZufEFnBJGSMPHhRY00hlJwA7Ah74My7AnyllIehmhY1Awlh6kiJrAzD6p05gCcOXcGFIdBHr1UeQLm7cniCk5L5Q4PDMAO7BkZzcJFBx3iFeAkJUgQBK4KSiTF5Y-qFUFKhw4FE50AhsBUXKPGGQza2i4pLS1fQwyu3w9u2oygoYrf69aeEZTZGB8Z5FoSvgwoGuSeApc7sUVHhwsxHEFPv2U6fcLW0dqQDmCTuvSrXM9l7rYIoi-n8qPp-AYIHUkAAFAASAEEAMoAUSC63IVFIajCVSiATSPz+KKxWwSqJe7iogiWxKx6NaJMpOyuVJyjRIDwQhXAdyK4lw0V6BhgvQUSkgXw0CHZnCQ0ycrlZC3ZRQ5MqJ8t4-B86uxMXiao5as2aUVCo5jMCSn0xsZan8dwoAHkAKoAFWYzzVf3lSlEzIA9piRFFUPgENxoOjZHBcJZpSALhR8NQjhxmEA

After tons of trial and error, I finally designed a simple but effective system that can shift phase up to 1080° (three full 360° rotations). Based on my analysis of various synths, that’s more than enough to create deep modulations and complex timbres.

![1](https://github.com/user-attachments/assets/809f5ae6-09f3-4d24-bfaa-d2cc60eb9987)

I designed the oscillator stay in tune in a wide range of temperatures (16-40°) using a thermistor, cermet trimmers and NP0 capacitors.

![3](https://github.com/user-attachments/assets/0741ba0a-dae5-40de-8d5b-746bfd7262bb)

https://www.amazon.co.uk/PATIKIL-Thermistors-Resistors-Sensitivity-Temperature/dp/B0CH1FM45S/ref=sr_1_42?crid=2PO48K8B9DAVM&dib=eyJ2IjoiMSJ9._iAXf_s02NVtFBTOVJ6MGLlBHIxLvBZRSsyGjO65-eNUYbOO841gfefq2N8tQ-3XPFiIvvaHtI_lKhbFadjllNfpF1H1fk5MepMWPowvv4YdZVB8iMPl0V9ZihQQxlg5YEDgEw-vlig2NqiWXd0_CfUpDPVC-raveck4wm_7CkPWm9xzcdTNBiIqjot47SAJzjcLHdjV9xOP5PB6jmtMQcUvj0gEPlgNqe_9yV8hDN4-IjDP3danrVYsn2z54oD8X1tt7e3-gw4YDRc0x0MroDHD4hW6vxcDCw--xL_NhR4fHCU174P-9IlphG002W45QIrJHR9xngUFX7-4C1s6OzYYsu7cBSqQmvKN8a8oaydgYJCYaRg-erTR4S-QU37IrFpfOwOqaAqGgkTBiO8ZI9m94ymAEoCiNy8GpVSsCuUGIlo35vrb23mubh_as85P.22cStzWStvYKLB36kP36bqlTu9OjEy7Ady04mHiY0bY&dib_tag=se&keywords=thermistor&qid=1738762674&sprefix=thermistor%2Caps%2C105&sr=8-42&th=1

The code for the MIDI interface is available here:
https://github.com/PaoloEstorm/MIDI-to-CV

PCB Design Here:
https://oshwlab.com/estorm/origami
