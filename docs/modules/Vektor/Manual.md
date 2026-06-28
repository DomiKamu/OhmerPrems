# VEKTOR & VX: USER'S MANUAL (UNDER CONSTRUCTION)


_They're all 8 models (GUI theme variations) for Vektor and its right-side attached VX expander modules:_
![](_img/AnimVektorModels.gif)


### TOPICS

- [**HISTORY OF THE VECTOR SYNTHESIS**](#history)
- [**INTRODUCTION**](#intro)
- [**MODULES SPECIFICATIONS**](#specs)
- [**DISCLAIMER: VCV RACK 2 "PRESET" LIMITATIONS**](#presetlimitation)
- [**VEKTOR MODULE LAYOUT**](#layoutvektor)
- [**VX EXPANDER MODULE LAYOUT**](#layoutvx)

---

### HISTORY OF THE VECTOR SYNTHESIS<a name="history"></a>

Welcome into the **Vector Synthesis** universe!

_Vektor_ is a 16HP polyphonic digital VCO module, using [**Vector Synthesis**](https://en.wikipedia.org/wiki/Vector_synthesis) technology (often abbreviated as **VS**) conceived by Sequential Circuits company for [**Prophet VS**](https://en.wikipedia.org/wiki/Prophet_VS) synthesizer (manufactured from 1986). Unfortunately, this innovative form of synthesis did not meet with great success, probably due to the high price of the Prophet VS synthesizer during this epoch (approx. USD 9,000 after 2026 conversion!).

_This is the 1986 Prophet VS synthesizer, manufactured by Sequential Circuits:_
![](_img/Prophet_VS.png)

When the Sequential Circuits went bankrupt during 1987, the company was sold to Yamaha, who have developed the SY22, SY35, and TG33. Then later (mid-1989), Dave Smith, the founder of Sequential Circuits company, have started the Korg USA R&D department, which went on to produce the [**Korg Wavestation**](https://en.wikipedia.org/wiki/Korg_Wavestation) synthesizer, also using Vector Synthesis but... as advanced, mainly due to extra feature named _Wave Sequencing_ (useful to create evolving sounds).

During 2015, Yamaha had returned the original trademark to **Dave Smith Instruments** (prior to be rebranded as **Sequential**, three years later).

Notable artists who have used the Prophet VS synthesizer was Depeche Mode, Vangelis, Brian Eno, Prince, Kraftwerk, Erasure, Rush, French singers Michel Berger and Christophe, and filmmaker John Carpenter.

---

### INTRODUCTION<a name="intro"></a>

Partially inspired by the Behringer [**Victor**](https://www.behringer.com/en/products/0720-ADA) Eurorack module, the objective of _Vektor_ module is to provide the "VCO parts" of the Prophet VS synthesizer, including the famous mixer joystick (for dynamic waveform crossfading) inside "the diamond", and its MIXing ENVelope who is working like an "automation curve" (in most modern DAWs) to control the waveform crossfading automatically.

Also provided by _Vektor_, two internal (independent) low-frequency oscillators (**LFO 1** and **LFO 2**), plus **FM input** jack, able to work as either **TZ FM** (linear Through-Zero FM) or **PM** (Phase Modulation, variant of FM synthesis used by Yamaha DX synthesizers family). These possible **frequency modulators** are designed to modulate any sound source (waveform) you'll want (OSC A, B, C or D), offering near infinite possibilities to a sound designer. LFO 1 and/or LFO 2 can be used by other modules in your rack, by attaching the _VX_ expander alsongside _Vektor_.

However, many parts of the real Prophet VS, like analog filters, ADSR envelope generators, stereo field/panning, and chorus, aren't provided by the _Vektor_ module, assuming they're a lot of third-party modules capable to do similar job inside our virtual Eurorack modular environment! By this way, when used "alone", _Vektor_ module cannot be considered as ready-to-use synth voice module!

_Vektor_ is using four independent oscillators (waveforms), named **OSC A**, **OSC B**, **OSC C** and **OSC D** (or by simple letters **A**, **B**, **C**, and **D** also refer to respective OSC A, OSC B, OSC C, and OSC D), as sound sources. Both of them are mixed (crossfading) either manually by the joystick (the "diamond"), by external voltages (applied to **X** and **Y** input jacks), or via fully automated **MIX ENV**elope (controlled by **GATE** input jack).

Each oscillator uses single-cycle sample, named **waveform**, like the real Prophet VS hardware synthesizer does. The 96 official waveforms are provided as "built-in ROM", numbered from **032** to **127**, have a name and graphical representation from oscillator context (first page). Please notice the built-in waveform number **126** (named **SILENCE**), when selected, the related oscillator isn't processed by the DSP, also waveform number **127** is constant-frequency **WHITE NOISE**.

:warning: Built-in **126. SILENCE** waveform, when selected for a particular oscillator (A, B, C, or D), doesn't provide extra "pages", because it's a nonsense to set frequency and/or volume for silent/muted oscillator! In this case, the **PAGE** button has no effect. Also, built-in **127. WHITE NOISE** waveform provides only **OSC VOLUME** as extra page, but not **OSC FREQUENCY**, because white noise frequency is constant (it doesn't follow V/OCT input), and cannot be modulated by FM/PM or by internal LFO.

The _Vektor_ module permits to import custom WAVE (.wav) file to any **USER waveform** slot (numbered from **000** to **031**, respectively labelled **USER #1** to **USER #32**). WAVE file importation will be explained later (having a dedicated section in this User's Manual).

As module outputs, the most important is **MIX** (always post-joystick or post MIX ENVelope), but they're also **A**, **B**, **C**, and **D** discrete oscillator outputs (useful for particular FX processings). Every discrete OSC output may be either **post-joystick** (or post MIX ENVelope) - it's the default behavior, or **pre-joystick** (or pre MIX ENVelope) like "dry" (unmixed).

Every output jack delivers a **mono audio signal** (10V peak-to-peak, -5V/+5V range, polyphonic when required), can be sent to mixer (or VCV AUDIO) module, to another module for FX processing, or as modulation source for other module in your rack (FM, AM, envelope follower, ring modulator, any you'd like in fact).

_Vektor_ module comes with (optional-to-use) 3HP "right side" expander, named _VX_ (accronym of **V**ektor e**X**pander), offering seven additional outputs:
- **LFO 1** and **LFO 2** (top section), each outputs the related (and configured) LFO signal (-5V/+5V range, can be sine, triangle, sawtooth, ramp, square or random).
- **JOY X** and **JOY Y** (middle section) who report respectively the X (horizontal) and Y (vertical) position of the **physical joystick**.
- **GATE** (bottom section) who outputs +10V while the MIX ENVelope is running (its LED is blue), 0V otherwise (its LED is unlit).
- **ENV X** and **ENV Y** (bottom section) who report the X and Y positions of the running MIX ENVelope (envelope point #4/release position, otherwise).

Vektor VCO module is polyphonic, up to 16 voices (channels). However, please be careful about CPU load as soon as you increase polyphony setting from the source module(s), please keep in mind 16 polyphonic channels x 4 oscillators, plus two LFO, plus the MIX ENVelope who are using Pythagorean and trigonometric sin/cos functions to establish trajectories) may require an important amount of CPU resources. Recommended polyphony setting for _Vektor_ module is 4, or 8 voices.

---

:information_source: The best for the end, _Vektor_ and _VX_ modules are free for everyone (license V2 keyfile is not required)!

---

### MODULES SPECIFICATIONS<a name="specs"></a>

_Vektor_ module technical specifications:

- Designed for VCV Rack 2 (v2.6.6, or higher), "Free" and "Pro" editions.
- Width: 16HP.
- Available models (GUI theme variants): 8 (please watch the animation at the top of this page, for available models).
- Display: **non-touchscreen** OLED (blue).
- 5 "context" momentary buttons OSC A, OSC B, OSC C, OSC D, MIX, overlooked by horizontal red LED "bars".
- 5 left-side momentary buttons L1 to L5.
- PAGE momentary button.
- DATA ENTRY continuous encoder.
- Polyphony: yes (max. 16 polyphonic voices/channels).
- Sound sources: 4 (OSC A, OSC B, OSC C, and OSC D), using waveforms/samples.
- Built-in ROM waveforms: 96, including "silence" (disabled OSC), and constant-frequency white noise.
- User waveforms: max. 32 (per module instance).
- LFO: 2 internal (separate) LFO 1 and LFO 2, per program.
- LFO frequency range: min. 0.01Hz, max. 50Hz, resolution 0.01Hz, default 2Hz.
- LFO AMPlitude range: min. 0% (LFO is turned off), max. 100% (+5V).
- LFO waveforms: sine, triangle, sawtooth, ramp (inverted sawtooth), square, random.
- Joystick: manual A/B/C/D volume crossfading, MIX ENVelope points editing.
- MIX ENVelope (automated A/B/C/D mixing): yes, fully customizable, controlled by GATE, per program.
- MIX ENVelope points: 5 (point 0 is start, point 3 is sustain, point 4 is release).
- MIX ENVelope rates: 4 (times in milliseconds, min. 0ms, max. 5000ms).
- MIX ENVelope loop.
- Input jacks: 7 (V/OCT, joystick X, joystick Y, GATE, VEL, FM).
- Supported FM modes: linear Through-Zero (TZ FM), Phase Modulation (PM). Per program.
- OSCillators modulation: by external FM/PM, by internal LFO 1, by internal LFO 2. Per oscillator, per program.
- Output jacks: 5 (MIX, A, B, C, D).
- Output voltage ranges: -5V to +5V.
- Stereo: none (all outputs are mono).
- Programs: 16.
- RGB LED: no (single colored LEDs, for inputs: yellow for V/OCT, blue for GATE, green for VEL and FM).
- Operational sample rate: recommended 44100Hz and higher.
- Self-test feature: on first installation in rack, on full reset to default factory.

_VX_ expander module technical specifications:

- Designed for VCV Rack 2 (v2.6.6, or higher), "Free" and "Pro" editions.
- Width: 3HP.
- Must be placed alongside the **right side** of any _Vektor_ module, **without space** between them.
- Available models (GUI theme variants): 8, automatically follows the _Vektor_ module's model when linked.
- Outputs: 8 (LFO 1, LFO 2, JOY X, JOY Y, GATE, ENV X, ENV Y).
- Output voltage ranges: -5V to +5V.
- LED: per output, all RGB.

---

### DISCLAIMER: VCV RACK 2 "PRESET" LIMITATIONS<a name="presetlimitation"></a>

:warning: Due to **huge amount of datas by using custom WAVE files as USER waveforms** (each supported WAVE file is **4140 bytes filesize** (approx. 900 kilobytes when all 32 user slots are loaded by external .wav files, so it's too large for reasonable and reliable json serialization), and the unavailability of "patch storage" for preset files (.vcvm) is really problematic - unfortunately, it's a (weird) VCV Rack 2 limitation - when you save the module's state as **VCV Rack 2's "Preset"** in case the current module instance includes user waveform(s), because these waveforms are lost/missing on open/recall by the preset file, later! Also, VCV Rack 2 doesn't provide specific API functions to distinguish between preset and regular patch file! Many developers are stucked about these unbelievable software limitations.

**So, please proceed with caution about VCV Rack 2's "Preset" files if you're using USER waveform(s)!**
Except user waveforms, all other module datas are 100% "Preset" compatible, however.

In case of problems about user waveforms, please contact support@vcvrack.com to request a "patch storage" per preset profile! I'll do not provide any technical support concerning this fact, because I'm not responsible. Thanks in advance for your understanding!

---

### VEKTOR MODULE LAYOUT<a name="layoutvektor"></a>

Section in under construction...

---

### VX EXPANDER MODULE LAYOUT<a name="layoutvx"></a>

Section in under construction...

---

...TO BE CONTINUED... THANKS FOR YOUR PATIENCE! ;)