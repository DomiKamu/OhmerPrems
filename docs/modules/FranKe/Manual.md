**FRANKE MODULE - SPECIFICATIONS & QUICK GUIDE**

![](_img/FranKe.png)

As "kind of complement" of _FroeZe_ trigger-based sequencer (mainly from drums), _FranKe_ module is a 80HP quantized note-based sequencer, as requested by an (old) OhmerPrems member!

_FranKe_ (also a tribute to Christopher Franke, member of Tangerine Dream band) is providing 64 patterns, 8 tracks per pattern, 16 steps per track.

Track 8 may be replaced by a powerful 16-bit Turing Machine (state is always saved/recalled). In this case, the previous content of track 8 is hidden, and fully restored in case you close the Turing Machine.

:warning: **Note-based track 8 and Turing Machine (also using track 8) cannot be used at the same time!**

Each track have its own **PITCH**, +10V **GATE**, and (optional to use) **VELOCITY** output jacks.

:warning: **FranKe module is not an instrument**, but a voltage-based sequencer, who sends voltages in order to control other modules:
- **PITCH** to any sound source module, like oscillator (VCO), synth voice, sampler, etc... who have **V/OCT** (or **PITCH**) input jack.
- **GATE** who output 0V or +10V gate voltage, mainly to control an envelope generator, or similar.
- **VEL.** (usage is optional), who output additional control voltage regardling the velocity.

- Like future (in development) 6OP-DX synth voice module, 8 models (GUI theme variations) are available, like most Ohmer & OhmerPrems modules: compliant with **Prefer dark panels if available** feature (from **View** menu, since VCV Rack v2.4.0). Existing models are **Aluminium** (it's the default model if _Prefer dark panels if available_ option is disabled), **Stage Repro**, **Cobalt**, **Absolute Night** (it's the default model if _Prefer dark panels if available_ option is enabled), **Dark "Signature"**, **Fort Knox "Signature"**, **Oxide "Signature"**, and **Titanium "Signature"**. All "Signature" models embed gold metal jacks, buttons, and screws (instead of silver metal for non-"Signature" line). Obviously, all models are providing exactly the same features!

:warning: FranKe module is under development, it will be available soon...

----

Free version (without license V2 keyfile) is working as **full player** (patches made by OhmerPrems member can be used without any restrictions). Without license V2 keyfile, **only track 1 can be edited** (any pattern), other note-based tracks (2 to 8) are locked (bottom **STEP** and **TRACK 2** - **TRACK 8** continuous encoders are inoperative on all these tracks). However, the _Turing Machine_ (using track 8, as alternate) is fully usable without any restriction (all parameters can be changed). All stuff is always saved and recalled.