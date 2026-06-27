# VEKTOR & VX: USER'S MANUAL (UNDER CONSTRUCTION)


![](_img/AnimFranKeModelsV2.gif)


### TOPICS

- [**INTRODUCTION**](#intro)

---

### INTRODUCTION<a name="intro"></a>

Welcome in the Vector Synthesis (VS) world!

Vektor module is a 16HP digital polyphonic VCO, using Vector Synthesis, a concept conceived and developed by Sequential Circuits (Dave Smith) during 1986, for the Prophet VS synthesizer. Unfortunately, this form of synthesis did not meet with great success, probably due to the high price of the Prophet VS.

When the Sequential Circuits company went bankrupt, its founder, Dave Smith, was recruited by Yamaha, then by KORG. Dave Smith have developed the KORG Wavestation, a synthesizer who are using Vector Synthesis technology, and by adding amazing features like sequenced sounds.

The objective of Vektor module is to provide the VCO part of these synthesizers, including the mixer joystick, the automated mixing envelope, two internal LFOs, and a FM input able to work as **TZ FM** (linear Through-Zero FM) or as **PM** (phase modulation, like Yamaha DX7 synth is using).

Vektor uses four independent oscillators, named A, B, C and D, as source sounds, can be mixed either manually by the joystick, 

Each oscillator part uses samples (96 are provided as "built-in ROM-like", from 032 to 125, #126 is "silence", and #127 is white noise). However, the end user (you!) can import a .wav file to any user waveform "slot" (from 000 to 031, as USER #1 to USER #32).

Vektor module comes with an 3HP "right side" expander, who provides only outputs:
- LFO 1.
- LFO 2.
- JOY X and JOY Y, who report the X (horizontal) and Y (vertical) position of the physical joystick.
- ENV X and ENV Y, who report the X and Y position of the MIX ENVelope (while running).
- GATE, set @ +10V while the MIX ENVelope is running, 0V otherwise.
