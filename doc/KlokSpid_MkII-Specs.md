**KLOKSPID MKII MODULE SPECIFICATIONS**

This **16HP** versatile clock source, named **KlokSpid MkII**, as successor of 2017 KlokSpid module from free Ohmer plugin. This module is:

- Clock generator, clock modulator (slave mode, when CLK input is patched to another clocking source).

- Up to 8 separate outputs. By default outputs 1-4 are active (pulse 1ms, amplitude 10V, offset 0V, in-phase, x1 ratio), other outputs 5-8 are turned off to save CPU (can be turned on, via Select Output menu > output clickable box > Modifier).

- For each output, they're **utility modifiers**, such GATE (send +5V/+10V high-state gate while clock is running), START (send 1ms +5V/+10V unique pulse when clock is started), STOP (send 1ms +5V/+10V unique pulse when clock is stopped), and OFF (output is totally disabled, send constantly 0V, internal processing are disabled).

- Up to 8 inputs: CLK (can become bipolar -5V/+5V, or unipolar 0V/10V **CV1** input), RUN (can become bipolar -5V/+5V, or unipolar 0V/10V **CV2** input). Native CV3 can become **RESET** instead (useful to reset/realign all internal phases), and CV4 to CV8 (default bipolar -5V/+5V, or unipolar 0V/10V).

- Output waveform can be PULSE, TRIANGLE (including ramp down and ramp up), SINE (including half sine and humps), Sample & Hold, CONTINUOUS voltage, ALARM (first pulse when clock is started, second last pulse on next beat - BPM x ratio), LIN/LOG and LIN/EXP envelope generators, and 8 possibles custom wavetables (at the moment .wav **Xfer Serum-compliant** wavetable files will be supported).

- Controllable by encoder + SET (blue) button + Cancel button combo, and touchscreen.

- As master clock, possible BPM is from 1 upto 900 (under consideration to increase, by using **frequency in Hz** beyond BPM 900). Can be set by encoder only.

- Many pre-built clocking ratios, including exotic even/prime/decimal dividers, from slowest /16384, to fastest x128. Pre-built ratio can be selected by any valid CV source.

- CV input can be manually set as bipolar -5V/+5V (default) or unipolar 0V/10V, via input on-screen menu.

- Output voltage supports **Amplitude** setting (min. 0.2V, max. 10V), can be modulated by any CV source. An option (via context menu) permits to force amplitude to 20V (-10V/+10V range), per output.

- Each output can receive a particular ratio, _'morphable'_ waveform (depending waveform type, morph have different name, such P-Width for pulse, Tilt for triangle, Deform for sine, Density for S&H, Attack for envelopes, WT-Pos for wavetables), voltage amplitude, voltage offset (amplitude can be above offset, or centered around offset), phase shift (from -180° to +180°), user-defined (or default) setting may be modulated by any CV source.

-   Before output to relevant jack, the voltage crosses bypassable **Euclidean sequencer** (user-defined settings, CV controllable), then bypassable pitch-based **Quantizer** (notes on/off aren't CV controllable, however). Either the clock (transport) is running, or stopped.

- An option permits to output the module's master phase to output 8 (ramp up signal shape, 0V to +10V, based on master tempo - clock / slave BPM). May be useful for rack debugging features, time reference...

- Six models (GUI theme variations) like most Ohmer & OhmerPrems modules. Compliant with **Prefer dark panels if available** feature (from **View** menu - since VCV Rack v2.4.0).

This module is absolutely free for everyone (even for non-OhmerPrems members).
