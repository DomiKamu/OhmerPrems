**KLOKSPID MKII MODULE SPECIFICATIONS**

This **16HP** versatile clock source, named **KlokSpid MkII**, will be the successor of _2017 KlokSpid_ module, offered by Ohmer (free / open source) plugin. Typically, this module is:

- Totally free, all features are available for everyone, including non-OhmerPrems members!

- "CPU-controlled"-like versatif clock generator (standalone), or clock modulator (slave mode, when CLK input is patched to another clocking source), including a main touchscreen-like display, plus an info display below the continuous encoder, usable as low-frequency oscillator (LFO), BPM-based envelope generator, optional (per-output) euclidean rhythms, and optional pitch quantizer.

- All embedded LED on module's chassis are RGB.

- 8 independent outputs. Please notice by default outputs 1-4 are active (pulse 1ms, amplitude 10V, offset 0V, amplitude above offset, in-phase, BPM x1 ratio), "a contrario" outputs 5-8 are turned off (their LED are lit, red color) in order to save CPU. Any output you want can be turned on, obviously, depending your needs, via touchscreen **Select Output** menu, then output # clickable box (the output becomes current for parameter editings), then **Modifier** menu item.

- For each output, they're special modifiers, named **utility modifiers**, such **GATE** (send constant +5V or +10V high-state gate while the clock is running, 0V when stopped), **START** (send short 1ms +5V or +10V pulse as soon as the clock is started), **STOP** (send short 1ms +5V or +10V pulse as soon as the clock is stopped), may be useful to control external modules such sequencer, switches... **OFF** shutdown the output - it sends 0V constantly (all internal processings are bypassed). Most usage are 1 to 4 outputs, it's the reason why - by default - the extra outputs 5-8 are natively disabled.

- Up to 8 inputs: **CLK** is designed to receive voltage from another clocking source. This input can be turned to bipolar -5V/+5V, or unipolar 0V/10V **CV1** input, in case you'll need extra CV inputs). RUN input can become bipolar -5V/+5V, or unipolar 0V/10V **CV2** input. Native CV3 can become **RESET** input instead, useful to reset/realign all internal phases. Finally they're extra CV4 to CV8 (default **bipolar -5V/+5V**, optionally **unipolar 0V/10V**). Simply use **Select Input...** menu item from touchscreen to access a particular input to be configured.

- Output waveform (per output) can be either PULSE, TRIANGLE (including ramp down, ramp up, and "perfect" isosceles triangle, via _Tilt_ parameters), SINE (including half sine, and humps), Sample & Hold, CONTINUOUS OFFSET voltage (based on V-Offset setting, who can be modulated by any CV), ALARM (send first pulse on clock start, send second - but last - pulse on next beat, when 'BPM x ratio' is reached), LIN/LOG and LIN/EXP envelope generators, and 8 optional custom wavetables (at the moment, only 32-bit float IEEE .wav **Xfer Serum-compliant** wavetable files are supported, other formats will come later).

- The module can be controlled either by continuous encoder + **SET** (blue) button + **Cancel** button _"combo"_, and by touchscreen! However, some controls (like page arrows) are usable only by touchscreen.

- On displays, colorscheme is simple: cyan = selectable item. Yellow = current selection/active menu item/box, editing BPM, editing slave mode... Gray = disabled item (locked).

- As master clock, possible BPM is from 1 upto 900 (under consideration to increase, by using **frequency in Hz** beyond BPM 900). Can be set by encoder only.

- HINT: while modifying the clock BPM (by using the continuous encoder), doing a right mouse click on yellow indicated BPM returns to default BPM 120. While editing the clock BPM (or the slave mode), the parameter is automatically saved after 3-second timeout (auto-validation delay can be changed from **Global Settings** menu).

- As slave clock, possible sync modes are by received **pulse** trains on CLK input jack, by **PPQN** (unfortunately not stable/jitters on Windows rigs with USB audio interfaces), or by **BPM CV** (compatible behind Impromptu's CLOCKED module, who provide this feature!). Max

- 86 pre-built ratios, including exotic/even/prime/non-integer dividers/multipliers, from slowest **/16384**, upto fastest **x128**. These pre-built ratios can be picked - in realtime - by any valid CV source.

- CV input can be manually set as **bipolar -5V/+5V** (it's the default setting for all CV inputs for this module), or optionally set as **unipolar 0V/10V**, depending your needs, via input on-screen menu (Select Input, choose the relevant input by clicking its box). CV1-CV3 also can be changed "on-the-fly" via context menu (INPUT ROLES section).

- Output voltage supports customizable **Amplitude** setting (minimum 0.2V, maximum 10V), this setting can be modulated by any CV source. An option (via context menu, MISCELLANEOUS section) permits to force the amplitude to 20V (-10V/+10V range) for the current (selected) output - in this case, original settings are kept, but CV becomes useless on this output parameter.

- Each output can receive a particular ratio, _'morphable'_ waveform (depending waveform shape, 'morph' have specific alterate name, such _P-Width_ for pulse, _Tilt_ for triangle, _Deform_ for sine, _Density_ for sample & hold, _Attack_ for envelope generators, and _Morph_ for wavetables), voltage amplitude (default 10V), voltage offset (default 0V, amplitude can be above offset or centered around offset), phase shift (from -180° to +180° - except S&H doesn't have phase shift). User-defined (or default) settings may be modulated by any CV source.

- Before output the voltage to relevant jack, it may crosses (bypassable) **Euclidean sequencer** (user-defined settings, and CV controllable), then (bypassable) pitch-based **Quantizer** (however, notes on/off aren't CV controllable). Either the clock (transport) is running, or stopped!

- An option from context menu permits to output the module's master phase to output 8 (ramp up signal shape, 0V to +10V, based on master tempo - clock / slave BPM). May be useful for rack debugging features, time reference in your rack... When you enable this option, the previous output settings are saved, then restored when you disable this option.

- Transport (START/STOP) - LED is off while clock is stopped. LED is red while clock is running, controlled by button on module's chassis. LED is cyan while clock is running, controlled by RUN input.

- RUN input: when set as **HI-GATE** (default setting), the clock runs while a high gate voltage is applied on RUN input jack. When set as **RUN/STOP**, the input acts as transport toggle, everytime the jack receives a pulse (trigger), at least +0.2V rising front.

- RESET input: when the CV3 input is set as **RESET**, incoming +0.2V (rising front) pulse/gate will reset the main (master) module's phase, also all eight dedicated output phases.

- **UNDER CONSIDERATION:** a lot of "shortcuts" - by mouse clicking on **input-related LED** or **output-related LED**: for input LED, left click over will select the relevant input (it becomes the current input, for further parameters edit), then bring the configuration page. For output LED, left click over will select the relevant output (it becomes the current output, for further parameters edit), then open the output base menu. On the same way, **right mouse click** will display... voltage scope for relevant input or output!

- Input LED color scheme: cyan for pulses (triggers) / gates based inputs (CLK, RUN, and RESET). Green for CV-compliant voltages (in range), red if under-/over-voltage (outside range). Yellow for CLK only if set as BPM CV.

- Output LED color scheme: red if output is disabled (its modifier is set to "OFF"). Gradient green for regular output usage. Cyan for service voltage (its modifier is set to an "utility", like GATE, START, or STOP). Gradient purple (concerns output 8 only) if output 8 sends the master phase (the PHASE).

- All settings for current output can be copied to another output, by single operation (COPY menu item, from output base menu).

- All settings for current output can be "restored to default factory" (other outputs aren't affected). BE CAREFUL - **Initialize** command from module's context menu (or Ctrl+I, or Command+I on Mac platforms) will reset the module entirely (full reset).

- Six models (GUI theme variations) - like most Ohmer & OhmerPrems modules - are available (_Model_, from context menu, to select another one). Compliant with **Prefer dark panels if available** feature (from **View** menu - since VCV Rack 2 v2.4.0). Possible models are **Aluminium** (default if _Prefer dark panels if available_ global option is disabled), **Stage Repro**, **Absolute Night** (default if _Prefer dark panels if available_ global option is enabled), **Dark "Signature"**, **Fort Knox "Signature"**, and **Titanium "Signature"**.
