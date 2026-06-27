# VEKTOR & VX: USER'S MANUAL (UNDER CONSTRUCTION)


![](_img/AnimFranKeModelsV2.gif)


### TOPICS

- [**INTRODUCTION**](#intro)

---

### INTRODUCTION<a name="intro"></a>

Welcome into the **Vector Synthesis** (VS) universe!

Vektor is a 16HP digital polyphonic VCO module, using Vector Synthesis technology, conceived and developed by Sequential Circuits during 1986 for its Prophet VS synthesizer. Unfortunately, this particular form of synthesis did not meet with great success (probably due to the high price of the Prophet VS).

When the Sequential Circuits company went bankrupt during 1987, the company was sold to Yamaha. Then later, 1989, Dave Smith (founder of Sequential Circuits), have started the KORG USA R&D group, which went on to produce the KORG WAVESTATION synthesizer.

The objective of Vektor module is to provide the VCO part of these synthesizers, including the famous mixer joystick, the automated MIXing ENVelope, two internal LFOs, and a FM input able to work as **TZ FM** (linear Through-Zero FM), or as **PM** (Phase Modulation, like Yamaha DX synthesizers are using). However, some parts like filters and ADSR envelope generators, are not included, assuming other 3rd-party modules can do it! By this way, Vektor module can't be assumed, when used alone, as synthesizer voice!

Vektor uses four independent oscillators, named A, B, C and D, as source sounds, can be mixed either manually by the joystick, or via the automated MIXing ENVelope (triggered by GATE input jack).

Each oscillator part uses samples (96 official are provided as "built-in ROM-like", from #032 to #125). Please notice the built-in waveform #126 is "silence", and waveform #127 is constant-frequency white noise generator).

However, you can import WAVE (.wav) file to any USER waveform "slot" (from #000 to #031, as **USER #1** to **USER #32** waveform slots).

Vektor module give the **MIX** output (always post-joystick / post-MIX ENVelope), but also **A**, **B**, **C**, and **D** discrete outputs (for particular FX processing), each discrete output may be either post-joystick (or post MIX ENVelope) - as default behavior, or pre-joystick / pre MIX ENVelope (like "dry") audio signal.

Vektor module comes with (optional-to-use) 3HP "right side" expander, providing additional outputs:
- **LFO 1** and **LFO 2**.
- **JOY X** and **JOY Y**, who report the X (horizontal) and Y (vertical) position of the physical joystick.
- **ENV X** and **ENV Y**, who report the X and Y position of the MIX ENVelope (while running).
- **GATE**, who outputs +10V while the MIX ENVelope is running (0V otherwise).

Vektor VCO is polyphonic (up to 16 voices).
