**KLOKSPID MKII MODULE SPECIFICATIONS**

This **16HP** versatile clock source, named **KlokSpid MkII**, will be the successor of _2017 KlokSpid_ module (from Ohmer free plugin). This module is:

- Totally free, all features for everyone (even non-OhmerPrems members!).

- A "CPU-controlled"-like clock generator (standalone), or clock modulator (slave mode, when CLK input is patched to another clocking source).

- Up to 8 separate outputs. By default outputs 1-4 are active (pulse 1ms, amplitude 10V, offset 0V, in-phase, x1 ratio), other outputs 5-8 are turned off to save CPU (can be turned on, via Select Output menu > output clickable box > Modifier).

- For each output, they're **utility modifiers**, such GATE (send +5V/+10V high-state gate while clock is running), START (send 1ms +5V/+10V unique pulse when clock is started), STOP (send 1ms +5V/+10V unique pulse when clock is stopped), and OFF (output is totally disabled, send constantly 0V, internal processing are disabled).

- Up to 8 inputs: CLK (can become bipolar -5V/+5V, or unipolar 0V/10V **CV1** input), RUN (can become bipolar -5V/+5V, or unipolar 0V/10V **CV2** input). Native CV3 can become **RESET** instead (useful to reset/realign all internal phases), and CV4 to CV8 (default bipolar -5V/+5V, or unipolar 0V/10V).

- Output waveform can be PULSE, TRIANGLE (including ramp down and ramp up), SINE (including half sine and humps), Sample & Hold, CONTINUOUS voltage, ALARM (first pulse when clock is started, second last pulse on next beat - BPM x ratio), LIN/LOG and LIN/EXP envelope generators, and 8 possibles custom wavetables (at the moment .wav **Xfer Serum-compliant** wavetable files will be supported).

- Controllable by encoder + SET (blue) button + Cancel button combo, and touchscreen.

- As master clock, possible BPM is from 1 upto 900 (under consideration to increase, by using **frequency in Hz** beyond BPM 900). Can be set by encoder only.

- As slave clock, possible sync modes are by regular **pulses** train, by **PPQN** (but not stable/jerky on Windows rigs with USB audio interfaces), or by **BPM CV** (compatible behind Impromptu's CLOCKED module, who provide this feature!).

- Many pre-built clocking ratios, including exotic even/prime/non-integer dividers, from slowest **/16384** (ultra very slow LFO), to fastest **x128**. Pre-built ratio can be selected in realtime by any valid CV source.

- CV input can be manually set as **bipolar -5V/+5V** (default setting for all CV) or optionally **unipolar 0V/10V**, via input on-screen menu (CV1-CV3 also can be changed from context menu).

- Output voltage supports customizable **Amplitude** setting (min. 0.2V, max. 10V), this setting can be modulated by any CV source. An option (via context menu) permits to force amplitude to 20V (-10V/+10V range) for the current (last selected) output - in this case, original settings are kept, but CV becomes useless on this output parameter.

- Each output can receive a particular ratio, _'morphable'_ waveform (depending waveform shape, 'morph' have specific alterate name, such _P-Width_ for pulse, _Tilt_ for triangle, _Deform_ for sine, _Density_ for sample & hold, _Attack_ for envelope generators, and _Morph_ for wavetables), voltage amplitude (default 10V), voltage offset (default 0V, amplitude can be above offset or centered around offset), phase shift (from -180° to +180° - except S&H doesn't have phase shift). User-defined (or default) settings may be modulated by any CV source.

- Before output the voltage to relevant jack, it may crosses (bypassable) **Euclidean sequencer** (user-defined settings, and CV controllable), then (bypassable) pitch-based **Quantizer** (however, notes on/off aren't CV controllable). Either the clock (transport) is running, or stopped!

- An option from context menu permits to output the module's master phase to output 8 (ramp up signal shape, 0V to +10V, based on master tempo - clock / slave BPM). May be useful for rack debugging features, time reference in your rack...

- Six models (GUI theme variations) - like most Ohmer & OhmerPrems modules - are available (_Model_, from context menu, to select another one). Compliant with **Prefer dark panels if available** feature (from **View** menu - since VCV Rack 2 v2.4.0). Possible models are **Aluminium** (default if _Prefer dark panels if available_ global option is disabled), **Stage Repro**, **Absolute Night** (default if _Prefer dark panels if available_ global option is enabled), **Dark "Signature"**, **Fort Knox "Signature"**, and **Titanium "Signature"**.
