**KLOKSPID MKII MODULE SPECIFICATIONS**

This **16HP** versatile clock source, named **KlokSpid MkII**, will be the successor of _2017 KlokSpid_ module (from Ohmer free plugin). Typically, this module is:

- Totally free, all features for everyone (including non-OhmerPrems members!).

- A "CPU-controlled"-like clock generator (standalone), or clock modulator (slave mode, when CLK input is patched to another clocking source).

- Up to 8 independent outputs. By default, outputs 1-4 are active (pulse 1ms, amplitude 10V, offset 0V, amplitude above offset, in-phase, BPM x1 ratio). Outputs 5-8 are turned off (RED LEDs) to save CPU, can be turned on as your needs (via touchscreen **Select Output** menu, then output # clickable box, then **Modifier** menu item).

- For each output, they're special modifiers, named **utility modifiers**, such **GATE** (constant +5V/+10V gate while clock is running, 0V when stopped), **START** (short 1ms +5V/+10V pulse as soon as the clock is started), **STOP** (short 1ms +5V/+10V pulse as soon as the clock is stopped), and **OFF** (the output is totally disabled - it sends 0V constantly, all internal processings are ignored).

- Up to 8 inputs: CLK (can become bipolar -5V/+5V, or unipolar 0V/10V **CV1** input), RUN (can become bipolar -5V/+5V, or unipolar 0V/10V **CV2** input). Native CV3 can become **RESET** instead (useful to reset/realign all internal phases), and CV4 to CV8 (default bipolar -5V/+5V, or unipolar 0V/10V). Use **Select Input...** menu item from touchscreen to access a particular input to be configured.

- Output waveform can be PULSE, TRIANGLE (including ramp down, ramp up, and "perfect" isosceles triangle), SINE (including half sine and humps), Sample & Hold, CONTINUOUS voltage (based on V-Offset setting, modulable by CV), ALARM (first pulse on clock start, second - last - pulse on next beat, at 'BPM x ratio'), LIN/LOG and LIN/EXP envelope generators, and 8 optional custom wavetables (at the moment, only WAVE **Xfer Serum-compliant** wavetable files are supported, other layouts come later).

- Controllable either by continuous encoder + "SET" (blue) button + "Cancel" button combo, and by touchscreen! some controls (like page arrows) are usable by touchscreen only.

- On displays, colorscheme is simple: cyan = selectable item. Yellow = current selection/active menu item/box. Gray = disabled item.

- As master clock, possible BPM is from 1 upto 900 (under consideration to increase, by using **frequency in Hz** beyond BPM 900). Can be set by encoder only.

- HINT: while modifying the clock BPM (by using the continuous encoder), doing a right mouse click on yellow indicated BPM returns to default BPM 120. While editing the clock BPM (or the slave mode), the parameter is automatically saved after 3-second timeout (auto-validation delay can be changed from **Global Settings** menu).

- As slave clock, possible sync modes are by received **pulse** trains on CLK input jack, by **PPQN** (unfortunately not stable/jitters on Windows rigs with USB audio interfaces), or by **BPM CV** (compatible behind Impromptu's CLOCKED module, who provide this feature!).

- 86 pre-built ratios, including exotic/even/prime/non-integer dividers/multipliers, from slowest **/16384**, upto fastest **x128**. These pre-built ratios can be picked - in realtime - by any valid CV source.

- CV input can be manually set as **bipolar -5V/+5V** (it's the default setting for all CV inputs for this module), or optionally set as **unipolar 0V/10V**, depending your needs, via input on-screen menu (Select Input, choose the relevant input by clicking its box). CV1-CV3 also can be changed "on-the-fly" via context menu (INPUT ROLES section).

- Output voltage supports customizable **Amplitude** setting (minimum 0.2V, maximum 10V), this setting can be modulated by any CV source. An option (via context menu, MISCELLANEOUS section) permits to force the amplitude to 20V (-10V/+10V range) for the current (selected) output - in this case, original settings are kept, but CV becomes useless on this output parameter.

- Each output can receive a particular ratio, _'morphable'_ waveform (depending waveform shape, 'morph' have specific alterate name, such _P-Width_ for pulse, _Tilt_ for triangle, _Deform_ for sine, _Density_ for sample & hold, _Attack_ for envelope generators, and _Morph_ for wavetables), voltage amplitude (default 10V), voltage offset (default 0V, amplitude can be above offset or centered around offset), phase shift (from -180° to +180° - except S&H doesn't have phase shift). User-defined (or default) settings may be modulated by any CV source.

- Before output the voltage to relevant jack, it may crosses (bypassable) **Euclidean sequencer** (user-defined settings, and CV controllable), then (bypassable) pitch-based **Quantizer** (however, notes on/off aren't CV controllable). Either the clock (transport) is running, or stopped!

- An option from context menu permits to output the module's master phase to output 8 (ramp up signal shape, 0V to +10V, based on master tempo - clock / slave BPM). May be useful for rack debugging features, time reference in your rack...

- Six models (GUI theme variations) - like most Ohmer & OhmerPrems modules - are available (_Model_, from context menu, to select another one). Compliant with **Prefer dark panels if available** feature (from **View** menu - since VCV Rack 2 v2.4.0). Possible models are **Aluminium** (default if _Prefer dark panels if available_ global option is disabled), **Stage Repro**, **Absolute Night** (default if _Prefer dark panels if available_ global option is enabled), **Dark "Signature"**, **Fort Knox "Signature"**, and **Titanium "Signature"**.
