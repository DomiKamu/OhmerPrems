# VEKTOR & VX: USER'S MANUAL (UNDER CONSTRUCTION)


![](_img/AnimFranKeModelsV2.gif)


### TOPICS

- [**HISTORY OF THE VECTOR SYNTHESIS**](#history)
- [**INTRODUCTION**](#intro)

---

### HISTORY OF THE VECTOR SYNTHESIS<a name="history"></a>

Welcome into the **Vector Synthesis** (VS) universe!

Vektor is a 16HP digital polyphonic VCO module, using Vector Synthesis technology, conceived and developed by Sequential Circuits company during 1986, for its Prophet VS synthesizer. Unfortunately, this innovative form of synthesis did not meet with great success, probably due to the high price of the Prophet VS (approx. USD 9000, as 2026 conversion!).

When the Sequential Circuits went bankrupt during 1987, the company was sold to Yamaha. Then later (mid-1989), Dave Smith, the founder of Sequential Circuits company, have started the KORG USA R&D group, which went on to produce the KORG WAVESTATION synthesizer.

---

### INTRODUCTION<a name="intro"></a>

The objective of Vektor module is to provide the VCO part of synthesizers mentioned above, including the famous mixer joystick, and the automated MIXing ENVelope. Also provided two internal LFO (LFO 1, and LFO 2), and a FM input able to work as **TZ FM** (linear Through-Zero FM), or as **PM** (Phase Modulation, like Yamaha DX synthesizer family is using). However, some parts of these synthesizers, like filters and ADSR envelope generators, are not provided by Vektor module, assuming other third-party modules can do the similar job! By this way, when used alone, Vektor module cannot be assumed as "synth voice".

Vektor module is using four independent oscillators, named **OSC A**, **OSC B**, **OSC C** and **OSC D** (A, B, C, and D always refers to OSC A, OSC B, OSC C, or OSC D oscillator), as source sounds, both of them are mixed either manually by the joystick, by external voltages applied to **X** and **Y** input jacks, or via the automated **MIX**ing **ENV**elope (triggered by **GATE** input jack).

Each oscillator uses samples (96 official are provided as "built-in ROM", from #032 to #125). Please notice the built-in waveform #126 is "silence", and waveform #127 is constant-frequency white noise generator).

However, you can import WAVE (.wav) file to any USER waveform "slot" (from #000 to #031, as **USER #1** to **USER #32** waveform slots).

Vektor module give the **MIX** output (always post-joystick / post-MIX ENVelope), but also **A**, **B**, **C**, and **D** discrete outputs (for particular FX processing), each discrete output may be either post-joystick (or post MIX ENVelope) - as default behavior, or pre-joystick / pre MIX ENVelope (like "dry") audio signal (-5V/+5V, 10V peak-to-peak).

Vektor comes with (optional-to-use) 3HP "right side" expander, named **VX**, providing additional outputs:
- **LFO 1** and **LFO 2** in top section, each outputs the configured LFO.
- **JOY X** and **JOY Y**, middle section, who report the X (horizontal) and Y (vertical) position of the physical joystick.
- **GATE** (bottom section), who outputs +10V while the MIX ENVelope is running (0V, otherwise).
- **ENV X** and **ENV Y** (bottom section), who report the X and Y position of the MIX ENVelope (while running, point #4 positions otherwise).

Vektor VCO is polyphonic (up to 16 voices).

And the best for the end: both Vektor module and VX expander are totally free for everyone (license V2 keyfile isn't required).
