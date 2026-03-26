**FRANKE MODULE - SPECIFICATIONS & QUICK GUIDE (UNDER CONSTRUCTION)**

![](_img/FranKe.png)

As kind of complement of _FroeZe_ trigger-based sequencer (used mainly for drum machines, percussions and trigger outputs), _FranKe_ module is a 80HP analog sequencer, as requested by an (2019) OhmerPrems member!

_FranKe_ (a tribute to [Christopher Franke](https://en.wikipedia.org/wiki/Christopher_Franke), member of Tangerine Dream band during best-known lineup during mid-1970s) - is providing 64 patterns, 8 tracks per pattern, 16 steps per track.

Track may be melodic (by using notes, from C-1 to G9, with possible flat or sharp accidentals), or free CV voltages (named CV OUT) who can send any voltage of your choice, into -10V to +10V range (by 0.01V resolution).

Also, track 8 may be replaced by a powerful 16-bit Turing Machine (its state is always saved/recalled), common for all patterns. In this case, the content of melodic/CV OUT track 8 is preserved (and hidden), but fully restored as soon as you close the Turing Machine.

:warning: **Melodic/CV track 8 and Turing Machine cannot be used at the same time!**

This is a French-spoken 35min. [video](https://www.youtube.com/watch?v=BAPuK8xuvAo&pp=ygUNb2htZXIgbW9kdWxlcw%3D%3D) (the video have embedded English closed captions), from [Ohmer Modules channel](https://www.youtube.com/@OhmerModulesVCVRack) on YouTube. The video is, in first minutes, a quick tour of FranKe module, followed by detailled description of the Turing Machine feature.

Each track have its own **PITCH**, +10V **GATE**, and (optional to use) **VELocity** output jacks (However, the Turing Machine doesn't use velocities, so its **VEL.** output jack is disabled - its LED is lit as red).

:warning: **FranKe module is not an instrument**, but a voltage-based sequencer, who sends pitch voltages (V/Oct compliant) or free voltages, gates, and possibly velocities voltages, in order to control other modules such VCO, synth voice, enveloppe generator, VCA and so on:
- **PITCH** to any sound source module, like oscillator (VCO), synth voice, sampler, etc... who have **V/OCT** (or **PITCH**) input jack, or CV input of any module you'd like.
- **GATE** who output 0V or +10V gate voltages, mainly to control an envelope generator, or any module can be controlled by +10V gate voltage.
- **VEL.** (usage is optional), who output additional control voltage regardling the velocity triggered by related sequencer event.

Like future (still in development) [6OP-DX synth voice module](../6OP-DX/Manual.md), FranKe provides 8 different models (aka GUI theme variations), like most Ohmer & OhmerPrems modules: compliant with **Prefer dark panels if available** feature (from **View** menu, since VCV Rack v2.4.0). Existing models are **Aluminium** (it's the default model if _Prefer dark panels if available_ global option is disabled), **Stage Repro**, **Cobalt**, **Absolute Night** (it's the default model if _Prefer dark panels if available_ global option is enabled), **Dark "Signature"**, **Fort Knox "Signature"**, **Oxide "Signature"**, and **Titanium "Signature"**. All "Signature" models embed gold metal jacks, buttons, and screws (instead of silver metal for non-"Signature" line), and OLED-like touchscreens (instead of LCD touchscreens). Obviously, all models are providing exactly the same features!

:warning: FranKe module is under development, it will be available "soon" (planned to public around mid-April, or third week of April, 2026).

----

Free version (without license V2 keyfile) is working as **full player** (it can play any patch made by OhmerPrems member, without any restrictions). However, without a valid license V2 keyfile, **only track 1 and the Turing Machine can be edited, pattern 01 only** (exactly like FroeZe sequencer), all other tracks (and patterns from 02) are locked against edition, including "Randomize" in current pattern (from module's contextual menu / Ctrl+R / Command+R on Mac). All stuff made on _Franke_ module is always saved and recalled.

Due to limitation by VCV Rack 2, FranKe module doesn't support preset (.vcvm) and selection files (.vcvs), as long as onSave() and onAdd() C++ methods aren't supported for presets and module selections by the VCV Rack API.