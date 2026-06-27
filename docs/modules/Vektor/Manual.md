# VEKTOR & VX: USER'S MANUAL (UNDER CONSTRUCTION)


![](_img/AnimVektorModels.gif)


### TOPICS

- [**HISTORY OF THE VECTOR SYNTHESIS**](#history)
- [**INTRODUCTION**](#intro)
- [**MODULES SPECIFICATIONS**](#specs)
- [**DISCLAIMER: VCV RACK 2 "PRESET" LIMITATION**](#presetlimitation)
- [**MODULES LAYOUTS**](#layouts)

---

### HISTORY OF THE VECTOR SYNTHESIS<a name="history"></a>

Welcome into the **Vector Synthesis** (VS) universe!

Vektor is a 16HP digital polyphonic VCO module, using [**Vector Synthesis**](https://en.wikipedia.org/wiki/Vector_synthesis) technology (sometimes abbreviated as **VS**), conceived and manufactured by Sequential Circuits company, during 1986 for his Prophet VS synthesizer. Unfortunately, this innovative form of synthesis did not meet with great success, probably due to the high price of the Prophet VS synthesizer during its commercial period (approx. USD 9000, as 2026 conversion!).

_This is the 1986 Prophet VS synthesizer, by Sequential Circuits:_
![](_img/Prophet_VS.png)

When the Sequential Circuits went bankrupt during 1987, the company was sold to Yamaha. Then later (mid-1989), Dave Smith, the founder of Sequential Circuits company, have started the Korg USA R&D group, which went on to produce the [Korg Wavestation](https://en.wikipedia.org/wiki/Korg_Wavestation) synthesizer, also using Vector Synthesis but... as advanced because the Wavestation synthesizer had _Wave Sequencing_ extra feature.

---

### INTRODUCTION<a name="intro"></a>

The objective of Vektor module is to provide the VCO parts of Prophet VS mentioned above, including the famous mixer joystick, and the automated MIXing ENVelope. Also provided two internal separate low-frequency oscillators (**LFO 1**, **LFO 2**), plus **FM input** able to work as **TZ FM** (linear Through-Zero FM), or **PM** (Phase Modulation, like Yamaha DX synthesizers family is using). These possible modulators are designed to modulate the frequency of any sound source (OSC A to OSC D), offering ton of possibilities for sound design activity, and nearly infinite timbres!

:information_source: as traditional FM/PM complement, **RING MODULATION** is not implemented, but this feature is under consideration!

However, many parts like filters, ADSR envelope generators, and stereo field, are not provided by Vektor module, assuming many third-party modules can do the similar job, in Eurorack modular environment proposed by VCV Rack! By this way, when used alone, Vektor module cannot be considered as ready-to-use "synth voice"!

Vektor is constantly using four independent oscillators, named **OSC A**, **OSC B**, **OSC C** and **OSC D** (simple letters *A*, *B*, *C*, and *D* also refers to respective OSC A, OSC B, OSC C, or OSC D, obviously), as sound sources. Both of them are mixed either manually by the joystick, by external voltages (applied to **X** and **Y** input jacks), or via fully automated **MIX**ing **ENV**elope (controlled by **GATE** input jack).

Each oscillator uses single-cycle samples, named **waveform**, like the real Prophet VS hardware synthesizer does. The 96 official waveforms are provided as "built-in ROM", numbered from #032 to #125). Please notice the built-in waveform number #126 is "silence", and waveform number #127 is **constant-frequency** white noise generator). Built-in can be selected for any A/B/C/D oscillator, but can't be replaced by other.

However, you can import WAVE (.wav) file to any **USER waveform** slot (numbered from #000 to #031, labelled as **USER #1** to **USER #32**). WAVE file importation will be explained in dedicated section of this user's manual!

As module's outputs, obviously the most important is **MIX** (always post-joystick or post MIX ENVelope), but they're also **A**, **B**, **C**, and **D** discrete OSC outputs (useful for particular FX processings such delay, distortion, reverb, Leslie cab, compression, EQ, and so on), each discrete OSC output may be either post-joystick (or post MIX ENVelope) - as default behavior, or pre-joystick / pre MIX ENVelope (like "dry", aka not mixed).

Every output jack delivers a **mono audio signal** (10V peak-to-peak, -5V/+5V range, may be polyphonic).

Vektor module comes with (optional-to-use) 3HP "right side" expander, named **VX** (accronym of... **V**ektor e**X**pander), offering seven additional outputs:
- **LFO 1** and **LFO 2** (top section), each outputs the related (and configured) LFO signal (-5V/+5V range, can be sine, triangle, sawtooth, ramp, square or random).
- **JOY X** and **JOY Y** (middle section) who report respectively the X (horizontal) and Y (vertical) position of the **physical joystick**.
- **GATE** (bottom section) who outputs +10V while the MIX ENVelope is running (its LED is blue), 0V otherwise (its LED is unlit).
- **ENV X** and **ENV Y** (bottom section) who report the X and Y positions of the running MIX ENVelope (envelope point #4/release position, otherwise).

Vektor VCO module is polyphonic, up to 16 voices. Be careful, however, about CPU load when increasing polyphony setting of the source module(s).

Now the best for the end: both Vektor and VX expander are totally free for everyone (license V2 keyfile isn't required, the modules run as full unlimited).

---

### MODULES SPECIFICATIONS (VEKTOR, VX)<a name="layoutvek"></a>

The _Vektor_ module:

- Designed for VCV Rack 2 application/plugin (v2.6.6, and more recent), either Free and Pro editions.
- 16HP wide.
- 8 models (GUI themes), shown as animation at the top of this page!
- Follow the _Use dark panels if available_ VCV Rack 2 option, from module browser (_Aluminium_ for light, or _Absolute Night_ for dark panels).
- OLED blue display (**not a touchscreen**!).
- Five "context" momentary buttons (overlooked by "line-like" red LEDs), located below OLED display, to select a specific oscillator (A, B, C, or D), the MIX ENVelope context, or the PROGRAM context.
- Five lateral momentary buttons, used to select displayed parameter in front of.
- PAGE momentary button, to select next page (depending the context).
- DATA ENTRY continuous encoder (will be named "encoder" in tis user's manual, below), to change parameter (or to select another program).
- Polyphony: from 1 (mono) up to 16 voices.
- 4 sound sources: OSC A, OSC B, OSC C, and OSC D (also named respectively A, B, C, and D).
- 96 built-in (ROM) waveforms, including silence (no sound / disabled OSC) and white noise.
- Ability to import and use custom waveforms (32 slots are available).
- Supported WAVE file format: Microsoft/IBM WAVE specification, 44100Hz, signed 16-bit PCM, 2048 samples single cycle, mono (4140 bytes filesize).
- Two internal (independent) low-frequency oscillators: LFO 1, LFO 2.
- LFO frequency range: min. 0.01Hz, up to 50Hz (stepping by 0.01Hz).
- Available LFO waveforms: sine, triangle, sawtooth, ramp (inverted sawtooth), square, and random (Sample & Hold).
- Joystick, mainly used for manual mixing between oscillators. Also used to define the MIX ENVelope points.
- Optional MIX ENVelope feature (automated mixing), using five X/Y points (point 0 is start, point 3 is sustain, point 4 is release).
- MIX ENVelope rates (times in milliseconds required to reach the next point of the mix envelope).
- MIX ENVelope loop at sustain point (point 3): up to 12 repeats (or infinite), uni-/bi-directional, from point 3 to 2 / 3 to 1 / 3 to 0.
- V/OCT input jack, for VCO pitch (polyphonic, 1V/octave compliant).
- X and Y input jacks (physical joystick is ignored while **both jacks are connected** to external source). Operate at -5V/+5V range.
- GATE input jack, to control the MIX ENVelope, and the retrigger for LFOs.
- VEL (velocity) input jack, who accept -5V/+5V voltage range, to handle any oscillator's volume by incoming velocity voltage.
- FM input jack (can be set as linear Through-Zero FM, or as Phase Modulation), who accept -5V/+5V voltage range.
- MIX output jack (audio, mono, -5V/+5V range, polyphonic).
- Discrete/separate A, B, C, and D output jacks (audio, mono, -5V/+5V range, polyphonic, post-/pre-joystick / mix envelope).
- Each oscillator can be frequency-modulated by FM (TZ FM or PM, via FM input jack), by LFO 1, or by LFO 2.
- 16 programs (a program looks as synthesizer preset/patch). The first 15 are "factory demos", the PROGRAM #16 is INIT. All can be altered.
- The module is working at any samplerate (recommended: 44100Hz and higher).

The _VX_ expander module:

- Designed for VCV Rack 2 application/plugin (v2.6.6, and more recent), either Free and Pro editions.
- 3HP wide.
- To operate, this expander must be placed at the **right side of Vektor** module, **without space** between them.
- 8 models (GUI themes), automatically follow the Vektor module's theme (watch the animation at the top of this page).
- Follow the _Use dark panels if available_ VCV Rack 2's option, from module browser (_Aluminium_ for light, or _Absolute Night_ for dark panels).
- Two LFO output jacks (LFO 1, LFO 2), -5V/+5V voltage range.
- Two joystick-related output jacks (reporting X and Y positions), -5V/+5V voltage range.
- Two mix envelope output jacks (reporting X and Y positions), -5V/+5V voltage range.
- GATE output jack, who send +10V while the MIX ENVelope is running (otherwise, voltage is 0V, and its blue LED is unlit).
- Each output jack have its RGB LED. In normal operation, all LED are solid green, except GATE (solid blue, with _afterglow_).
- All LED **fast-blinking red** (as error condition) while the _VX_ expander is not linked to _Vektor_ module.

---

### DISCLAIMER: VCV RACK 2 "PRESET" LIMITATION<a name="presetlimitation"></a>

:warning: Due to **huge amount of datas** by using custom WAVE file(s) as USER waveform(s) (to USER slot, for #000 to #031), each supported WAVE file is 4140 bytes filesize (900 kilobytes, when all 32 user slots are using an external .wav file, it's too large for reasonable and reliable json serialization), and the unavailability of "patch storage" for preset files (.vcvm) - unfortunately it's a weird VCV Rack 2 limitation - when saving the module's state as VCV Rack 2 "Preset" if the module instance includes several user waveforms (because these user waveforms are lost/missing on open/recall the preset file, later).

So, please proceed with caution about VCV Rack's "Preset" files and USER waveform(s)!

In case of problem about this, please contact support@vcvrack.com to request "patch storage" for VCV Rack 2 preset files! Thanks for your understanding.

---

### MODULE LAYOUT (VEKTOR)<a name="layoutvek"></a>

Section in construction...

---

### EXPANDER MODULE LAYOUT (VX)<a name="layoutvx"></a>

Section in construction...

---

TO BE CONTINUED... THANKS FOR PATIENCE! ;)