**FRANKE MODULE - SPECIFICATIONS & QUICK GUIDE (UNDER CONSTRUCTION)**

![](_img/FranKe.png)

As kind of complement of _FroeZe_ trigger-based sequencer (used mainly for drum machines, percussions and trigger outputs), _FranKe_ module is a 80HP analog step-sequencer, as requested by an (2019) OhmerPrems member!

_FranKe_ (a tribute to [Christopher Franke](https://en.wikipedia.org/wiki/Christopher_Franke), member of Tangerine Dream band during best-known lineup during mid-1970s) - is providing 64 patterns, 8 tracks per pattern, 16 steps per track.

Tracks are versatile, any track may be "melodic" (by using notes, from C-1 to G9 with possible flat or sharp accidentals), free CV voltages (named CV OUT) who can send any voltage of your choice, into -10V to +10V range (by 0.01V resolution), or a 16-bit Turing Machine (common to all patterns).

By default as fresh module added in rack (or after **Initialize** from module's contextual menu / **Ctrl**+**I** / **Cmd**+**I** on Mac), track 1-5 are melodic (all steps filled filled by C4 notes), tracks 6 and 7 are **CV OUT** (to send sequenced modulations), track 8 is a Turing Machine.

To change a track role anytime, select the track either by touching its **TRACK encoder** or its **touchscreen**, then press **T. ROLE** (track role) button (located near CV1 input jack) to switch between roles (melodic -> CV OUT -> Turing Machine...)

Each track (line) have its own **PITCH**, +10V **GATE**, and (optional to use) **VELocity** output jacks, same row. However, **VEL.** output jack is disabled (its LED is lit as red, sends constant 0V) while the track role is set either by **CV OUT** or **Turing Machine**. VELocities are applicable only by melodic (notes).

:warning: **FranKe module is not an instrument**, but a voltage-based (analog) step-sequencer, who sends pitch voltages ("V/Oct" compliant) or free voltages, 0V/+10V gates, and possibly velocities voltages, in order to control other modules, such VCO, synth voice, enveloppe generator, VCA, and any module you'll want:
- **PITCH** to any sound source module, like oscillator (VCO), synth voice, sampler, etc... who have **V/OCT** (or **PITCH**) input jack, or CV input of any module you'd like.
- **GATE** who output 0V or +10V gate voltages, mainly to control an envelope generator, or any module can be controlled by +10V gate voltage.
- **VEL.** (usage is optional), who output additional control voltage regardling the velocity triggered by related note event (melodic track only, disabled otherwise).

Like future (still in development) [6OP-DX synth voice module](../6OP-DX/Manual.md), FranKe provides 8 different models (aka GUI theme variations), like most Ohmer & OhmerPrems modules: compliant with **Prefer dark panels if available** feature (from **View** menu, since VCV Rack v2.4.0). Existing models are **Aluminium** (it's the default model if _Prefer dark panels if available_ global option is disabled), **Stage Repro**, **Cobalt**, **Absolute Night** (it's the default model if _Prefer dark panels if available_ global option is enabled), **Dark "Signature"**, **Fort Knox "Signature"**, **Oxide "Signature"**, and **Titanium "Signature"**. All "Signature" models embed gold metal jacks, buttons, and screws (instead of silver metal for non-"Signature" line), and OLED-like touchscreens (instead of LCD touchscreens). Obviously, all models are providing exactly the same features!

:warning: FranKe module still under development, it will be available "soon" (planned to public around mid-April, or third week of April, 2026).

----

Free version (without license V2 keyfile) is working as **full player** (it can play any patch made by OhmerPrems member, without any restrictions). However, without a valid license V2 keyfile, **only track 1 and the Turing Machine can be edited, pattern 01 only** (exactly like FroeZe sequencer), all other tracks (and patterns from 02) are locked against edition, including "Randomize" in current pattern (from module's contextual menu / Ctrl+R / Command+R on Mac). All stuff made on _Franke_ module is always saved and recalled.

Due to limitation by VCV Rack 2, FranKe module doesn't support preset (.vcvm) and selection files (.vcvs), as long as onSave() and onAdd() C++ methods aren't supported for presets and module selections by the VCV Rack API.