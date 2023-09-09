**KLOKSPID MKII MODULE SPECIFICATIONS**

This **16HP** versatile clock source, named **KlokSpid MkII**, will be the successor of _2017 KlokSpid_ module, offered by Ohmer (free / open source) plugin. Typically, this module is:

- Totally free, all features are available for everyone, including non-OhmerPrems members!

- "CPU-controlled"-like versatif clock generator (standalone), or clock modulator (slave mode, when CLK input is patched to another clocking source), including a main touchscreen-like display, plus an info display below the continuous encoder, usable as low-frequency oscillator (LFO), BPM-based envelope generator, optional (per-output) euclidean rhythms, and optional pitch quantizer.

- All embedded LED on module's chassis are RGB.

- 8 independent outputs. Please notice by default (when you add a new instance of KlokSpid MkII module in your rack), only outputs 1 to 4 are active (default setting is pulse 1ms, amplitude 10V, offset 0V, amplitude above offset, in-phase, x1 ratio modifier). Outputs 5 to 8 have their LED lit as red, meaning they're turned off / disabled, in order to save CPU/resources. Of course, any output you want can be turned on (depending your needs) via touchscreen **Select Output** menu, then output # clickable box (the selected output becomes current for further parameters edits), then **Modifier** menu item. By using mouse (click on left or right arrow, top right side of display, to select previous/next page) or encoder/buttons, you can select another modifier for related output.

- For any output, it's existing special modifiers, named **utility modifiers**, such **GATE** who send constant +5V or +10V high-state gate while the clock is running (or 0V when stopped), **START** who send (once) a short 1ms +5V or +10V pulse (trigger) as soon as the clock starts), **STOP** who send (once) a short 1ms +5V or +10V pulse (trigger) as soon as the clock is stopped. These utility modifiers may be useful to control external modules. As indicated above, **OFF** simply shutdowns the output - it outputs 0V, constantly, all internal processings are bypassed. About clocking modules, major usages are 1 to 4 outputs, rarely more, it's the reason why the extra outputs 5-8 are natively disabled!

- 8 inputs: **CLK** is designed to receive voltages from another clocking source. When patched, the module becomes slave because the clock frequency or tempo depends of external module. This input can be turned to bipolar -5V/+5V, or unipolar 0V/10V **CV1** input, in case you'll need extra CV inputs. On the same way, **RUN** input can become bipolar -5V/+5V, or unipolar 0V/10V **CV2** input. Native CV3 (by default bipolar -5V/+5V CV input) can become a **RESET** pulse-based input, instead, it may be useful to reset/realign all internal phases. Finally, they're extra CV4-CV8 (default **bipolar -5V/+5V**, optionally **unipolar 0V/10V**). Simply use **Select Input...** menu item from _touchscreen_ to access a particular input to be configured.

- Output waveform can be either PULSE, TRIANGLE (including ramp down, and ramp up, via _Tilt_ parameter), SINE (including half sine, and humps), Sample & Hold (S&H), CONTINUOUS OFFSET voltage (based on V-Offset setting, who can be modulated by any CV), ALARM (send first pulse on clock start, then later send second - but last - pulse on next beat, when next 'BPM x ratio' is reached), LIN/LOG and LIN/EXP envelope generators, and 8 optional custom wavetables (at the moment, only 32-bit float IEEE .wav **Xfer Serum-compliant** wavetable files are supported, other formats will come later).

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
