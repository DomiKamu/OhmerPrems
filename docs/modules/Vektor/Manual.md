# VEKTOR & VX: USER'S MANUAL (UNDER CONSTRUCTION)


_They're all 8 models (GUI theme variations) for Vektor and its right-side attached VX expander modules:_
![](_img/AnimVektorModels.gif)


### TOPICS

- [**HISTORY OF THE VECTOR SYNTHESIS**](#history)
- [**INTRODUCTION**](#intro)
- [**MODULES SPECIFICATIONS**](#specs)
- [**DISCLAIMER: VCV RACK 2 "PRESET" LIMITATION**](#presetlimitation)
- [**MODULES LAYOUTS**](#layouts)

---

### HISTORY OF THE VECTOR SYNTHESIS<a name="history"></a>

Welcome into the **Vector Synthesis** universe!

_Vektor_ is a 16HP polyphonic digital VCO module, using [**Vector Synthesis**](https://en.wikipedia.org/wiki/Vector_synthesis) technology (often abbreviated as **VS**) conceived by Sequential Circuits company for his Prophet VS synthesizer (manufactured from 1986). Unfortunately, this innovative form of synthesis did not meet with great success, probably due to the high price of the Prophet VS synthesizer during this epoch (approx. USD 9,000 after 2026 conversion!).

_This is the 1986 Prophet VS synthesizer, manufactured by Sequential Circuits:_
![](_img/Prophet_VS.png)

When the Sequential Circuits went bankrupt during 1987, the company was sold to Yamaha. Then later (mid-1989), Dave Smith, the founder of Sequential Circuits company, have started the Korg USA R&D department, which went on to produce the [**Korg Wavestation**](https://en.wikipedia.org/wiki/Korg_Wavestation) synthesizer, also using Vector Synthesis but... as advanced, mainly due to extra feature: _Wave Sequencing_, to make evolving sounds.

During 2015, Yamaha had returned the original trademark to **Dave Smith Instruments** (then rebranded as **Sequential** during 2018).

---

### INTRODUCTION<a name="intro"></a>

The objective of Vektor module is to provide the "VCO parts" of the Prophet VS synthesizer, including the famous mixer joystick, and its automated MIXing ENVelope. Also provided by _Vektor_, two internal low-frequency oscillators (**LFO 1** and **LFO 2**), plus a **FM input** jack, able to work as either **TZ FM** (linear Through-Zero FM), or **PM** (Phase Modulation, used by Yamaha DX synthesizers family). These possible **frequency modulators** are designed to modulate any sound source you'll want (OSC A to OSC D), offering ton of possibilities for sound design, and rich palette of timbres!

However, many parts like filters, ADSR envelope generators, and "stereo field", aren't provided by Vektor module, assuming they're a lot of third-party modules can do the similar job in our virtual Eurorack modular environment! By this way, when used alone, Vektor module cannot be considered as ready-to-use _synth voice_ module!

Vektor is constantly using four independent oscillators, named **OSC A**, **OSC B**, **OSC C** and **OSC D** (simple letters *A*, *B*, *C*, and *D* also refers to respective OSC A, OSC B, OSC C, or OSC D, obviously), as sound sources. Both of them are mixed either manually by the joystick, by external voltages (applied to **X** and **Y** input jacks), or via fully automated **MIX**ing **ENV**elope (controlled by **GATE** input jack).

Each oscillator uses single-cycle samples, named **waveform**, like the real Prophet VS hardware synthesizer does. The 96 official waveforms are provided as "built-in ROM", numbered from #032 to #125). Please notice the built-in waveform number #126 is "silence", and waveform number #127 is **constant-frequency** white noise generator). Built-in can be selected for any A/B/C/D oscillator, but can't be replaced by other.

However, you can import WAVE (.wav) file to any **USER waveform** slot (numbered from #000 to #031, labelled as **USER #1** to **USER #32**). WAVE file importation will be explained below, in dedicated section of this user's manual!

As module's outputs, obviously the most important is **MIX** (always post-joystick or post MIX ENVelope), but they're also **A**, **B**, **C**, and **D** discrete OSC outputs (useful for particular FX processings such delay, distortion, reverb, Leslie cab, compression, EQ, and so on), each discrete OSC output may be either post-joystick (or post MIX ENVelope) - as default behavior, or pre-joystick / pre MIX ENVelope (like "dry", aka not mixed).

Every output jack delivers a **mono audio signal** (10V peak-to-peak, -5V/+5V range, may be polyphonic).

Vektor module comes with (optional-to-use) 3HP "right side" expander, named **VX** (accronym of... **V**ektor e**X**pander), offering seven additional outputs:
- **LFO 1** and **LFO 2** (top section), each outputs the related (and configured) LFO signal (-5V/+5V range, can be sine, triangle, sawtooth, ramp, square or random).
- **JOY X** and **JOY Y** (middle section) who report respectively the X (horizontal) and Y (vertical) position of the **physical joystick**.
- **GATE** (bottom section) who outputs +10V while the MIX ENVelope is running (its LED is blue), 0V otherwise (its LED is unlit).
- **ENV X** and **ENV Y** (bottom section) who report the X and Y positions of the running MIX ENVelope (envelope point #4/release position, otherwise).

Vektor VCO module is polyphonic, up to 16 voices. Be careful, however, about CPU load when increasing polyphony setting of the source module(s), please keep in mind 16 polyphonic channels x 4 oscillators, plus the MIX ENVelope who are using Pythagorean theorem & trigonometric functions (for trajectory) require more or less CPU resources.

:information_source: The best for the end, _Vektor_ and _VX_ modules are totally free for everyone (license V2 keyfile isn't required)!

---

### MODULES SPECIFICATIONS (VEKTOR, VX)<a name="layoutvek"></a>

The _Vektor_ module:

- Designed for VCV Rack 2 application/plugin (v2.6.6, and more recent), either Free and Pro editions.
- 16HP wide.
- 8 models (GUI themes), shown as animation at the top of this page!
- Follow the _Use dark panels if available_ VCV Rack 2's option (from View menu), inside the module browser (_Aluminium_ for light panels, or _Absolute Night_ for dark panels).
- OLED blue display (**not a touchscreen**!).
- Five "context" momentary buttons (overlooked by "line-like" red LEDs), located below OLED display, to select a specific oscillator (A, B, C, or D), the MIX ENVelope context, or the PROGRAM context (press the button where the LED is lit to access PROGRAM, all LED become unlit in this context).
- Five lateral momentary buttons, used to select displayed parameter (TIP: blinking "cursor" indicates the selected parameter).
- PAGE momentary button, to select next page, depending the context.
- DATA ENTRY continuous encoder (will be named "encoder" in this manual), to change selected parameter.
- Polyphony: from 1 (mono), up to 16 voices.
- 4 sound sources: OSC A, OSC B, OSC C, and OSC D (also named respectively A, B, C, and D).
- 96 built-in (ROM) waveforms, including "silence" (no sound + disabled OSC), and constant-frequency white noise.
- Ability to import/use custom waveforms (32 available slots), via dropping the .wav file over the OLED display, or right-click context menu.
- Supported WAVE file format: Microsoft/IBM "WAVE" specification, 44100Hz, PC signed 16-bit, 2048 samples, mono, single cycle (4140 bytes filesize). Other formats are not supported by _Vektor_ module!
- Two internal (independent) low-frequency oscillators: LFO 1 and LFO 2.
- LFO frequency range: min. 0.01Hz, up to 50Hz (stepping by 0.01Hz), 2Hz as default factory.
- LFO AMP range: min. 1%, up to 100%, to set the amplitude. At 0% the related LFO generator is turned off (not processed by the DSP).
- Available LFO waveforms: sine, triangle, sawtooth, ramp (inverted sawtooth), square, and random (Sample & Hold by integrated white noise).
- Joystick, mainly used for manual mixing between A/B/C/D oscillators. Also used to define the MIX ENVelope points.
- Optional MIX ENVelope feature (automated mixing), using five X/Y points (point 0 is start, point 3 is sustain, point 4 is release).
- MIX ENVelope rates (times in milliseconds required to reach the next point of the mix envelope).
- MIX ENVelope may loop at sustain point (point 3): up to 12 repeats (or infinite), uni-/bi-directional, from point 3 to 2 / 3 to 1 / 3 to 0. Loop feature is off by default.
- V/OCT input jack, for VCO pitch (polyphonic, 1V/octave compliant).
- X and Y input jacks (physical joystick moves are ignored while **both X and Y jacks are connected** to external source). Operate into -5V/+5V voltage range.
- GATE input jack, to control the MIX ENVelope, and the retrigger for LFOs. Minimum gate voltage is +1V (+10V is recommended for gates, however).
- VEL (velocity) input jack, accepting voltages into -5V/+5V range, to handle any oscillator's volume by incoming velocity voltage.
- FM input jack (can be set as linear Through-Zero FM, or as Phase Modulation), accepting voltages into -5V/+5V range.
- MIX output jack (audio, mono, -5V/+5V, polyphonic).
- Discrete A, B, C, and D output jacks (audio, mono, -5V/+5V range, post-/pre-joystick / mix envelope, polyphonic).
- Each oscillator can be frequency modulated by FM ("TZ FM" or "PM", via FM input jack), by internal LFO 1, or by internal LFO 2.
- 16 programs (a "program" looks as synth preset/patch). The first 15 are "factory demos programs", the PROGRAM #16 is INIT. All can be altered, saved, and so on.
- The module is working at any samplerate (recommended, for best results: 44100Hz and above).

The _VX_ expander module:

- Designed for VCV Rack 2 application/plugin (v2.6.6, or more recent), either "Free" and "Pro" editions.
- 3HP wide.
- To operate, _VX_ expander module must be placed alongside the **right side* of _Vektor_ module, **without space** between them!
- 8 models (GUI theme variants), automatically follow the _Vektor_ module's theme when placed alongside (watch the animation at the top of this page).
- Follow the _Use dark panels if available_ VCV Rack 2's option (from View menu), inside the module browser (_Aluminium_ for light panels, or _Absolute Night_ for dark panels).
- Two LFO output jacks (LFO 1, LFO 2), -5V/+5V voltage range.
- Two joystick-related output jacks (reporting X and Y positions), -5V/+5V voltage range, useful to control another module by the joystick.
- Two MIX ENVelope output jacks (reporting X and Y positions of the running mix envelope), -5V/+5V voltage range.
- GATE output jack, who outputs +10V gate while the MIX ENVelope is running (otherwise, voltage is 0V, and its blue LED is turned off).
- Each output jack have its (RGB) LED. In normal operation, all LED are solid green color, except GATE (solid blue instead, with _afterglow_ for very short gate durations).
- All LED are **fast-blinking red**, as error condition, while the _VX_ expander is not attached to _Vektor_ module!

---

### DISCLAIMER: VCV RACK 2 "PRESET" LIMITATION<a name="presetlimitation"></a>

:warning: Due to **huge amount of datas by using custom WAVE file(s) as USER waveform(s)**, each supported WAVE file is 4140 bytes filesize (900 kilobytes when all 32 user slots are loaded with an external .wav file, so it's too large for reasonable and reliable json serialization), and the unavailability of "patch storage" for preset files (.vcvm) - unfortunately this is a weird VCV Rack 2 limitation - when saving the module's state as **VCV Rack 2 "Preset"** in case the module instance includes user waveform(s), because these waveforms are lost/missing on open/recall by the preset file, later!

So, please proceed with caution about VCV Rack's "Preset" files and USER waveform(s)!

In case of problems about this, please contact support@vcvrack.com to request a "patch storage" per preset files! **I do not provide technical support concerning THIS PROBLEM** because I'm not responsible. Thanks in advance for your understanding!

---

### MODULE LAYOUT (VEKTOR)<a name="layoutvek"></a>

Section in construction...

---

### EXPANDER MODULE LAYOUT (VX)<a name="layoutvx"></a>

Section in construction...

---

TO BE CONTINUED... THANKS FOR YOUR PATIENCE! ;)