**FROEZE & FROEZE-X MODULES SPECIFICATIONS / QUICK GUIDE**

![](images/FroeZe_Header.png)

This **68HP** drum-based step sequencer, named **FroeZe** (in tribute to... Edgar Froese), is:

- 15+1 tracks (forming a pattern): 15 instrument tracks + separate **ACcent** track.

- Track naming follows _Roland_-style (for most of their vintage drum machines): **BD** for bass drum/kick, **SD** for snare drum, **CH** for closed hats... Obviously, except while audio engine is enabled (and particular AC track), track usage is free (it is not mandatory to follow instrument names for your project).

- 64 steps (max.) per track. LAST STEP (common to all tracks) is manually adjustable via dedicated encoder, and can be shifted (offset - / +) in real time via CV input jack, from minimum 1-step upto 64.

- Main display as "touchscreen"-like, mainly for note events editing (silences, notes, AC'd notes, or 8-preset defined ratchets), into 16x64 grid.

- FroeZe sequencer can deliver +10V 1ms triggers, (without FroeZe-X expander, for ac'd notes: **-10V** 1ms instead), or audio (thanks to internal QuadPercs engines).

- Any instrument track can be **SOLO**ed (except AC track). Multiple SOLO is possible.

- Any track can be **MUTE**d (including AC track). Multiple MUTEd tracks is possible.

- MUTE and SOLO can be used together on same instrument track (except AC track, can't be SOLOed).

- 128 patterns, each of them can be named. **Please follow displayed (OSD) instructions while (re)naming the current pattern!**

- Current pattern can be changed "on-the-fly by turning its encoder (clockwise to select next, counter-clockwise to select previous), via PREV./NEXT trigger input jacks, or absolute pattern number via CV (PREV. input jack + enabled "CV PATTERN" option via context menu). Any third-party trigger or CV sequencer can control pattern chaining (via triggers) or absolute (via voltages).

- LOOP: repeat current step (1/16), two-consecutive steps (1/8) or current bar (1/4) applied CV-voltage (gated) on LOOP input jack (+2V min. to +5V for 1/16, +5V to +9.99V for 1/8, +10V for 1/4). Unlike ratcheting note event, LOOP is applied on all playing tracks.

- LOOP via button (may be held): behavior (1/16, 1/8 or 1/4) can be defined via **"LOOP" button behavior** from context menu (default is 1/16 step repeat). Button is inoperative while a +2V (or more) is applied on LOOP input jack.

- REVerse pattern playback while REV. button is held, or via applied gate-voltage (held) on REV input jack (+2V min.).

- PENDULum pattern playback: playing forward from step 1 to track's last ste (left to right), then reverse back until step 1, then forward again... like a pendumum or ping-pong. Via applied & held gate-voltage on PENDUL. input jack (+2V min.). 

- Both REV and PENDUL. are usable together (non-loop).

- Both LOOP and REV are usable together (PENDULum is ignored while LOOP is active).

- %SWING CV input jack, with its mini display (below), to apply from 50% (meaning no swing) to 75% (max swing 1.5 - 0.5), applied in realtime on overall pattern. By using _left-side_ FroeZe-SX expander, this CV input is disabled (FroeZe-SX expander provides per-track discrete swings).

- Accent notes: outputs **-10V** (internal output jacks, **this requires Polarity Switch module** from freeware Ohmer Modules for alternate routing on negative voltages), **OR** by using **FroeZe-X** (12HP) expander, to bring 16 dedicated "accent output" jacks (plus some edit features).

- Notation in cells: **empty** means silence, **diamonds** for regular notes, **plain diamonds** for individual accent notes (regardless AC track), or 8-slot preset for ratcheting note patterns (symbol in grid - from top to bottom - is based on current ratchet preset, from slot #1 to slot #8).

- Ratcheting note is always based on **mandatory played 1st stage** (due to display limitation in cell), followed by 7-stage repeats (each of them can be enabled/disabled via editor in OSD context menu over related cell).

- AC track always uses empty or plain diamonds, to alter any note type located on the same step (same column) during playback.

- Smart OSD context menu (on right mouse click over a event cell, in grid). On right click over a ratcheting note, its 7-step pattern can be changed (left mouse clicks on relevant boxes!).

- **Under consideration**: SONG mode (incl. integrated song editor) -- Work In Progress, planned for v2.2.8...

- Smart track completion (applied on currently selected track), from FroeZe-X expander's TRACK page, or from OSD context menu.

- Basic euclidean rhythm (applied on selected track only), from FroeZe-X expander's TRACK / EUCLID. page. Track is entirely filled by indicated STEPS, NOTES (number of "hits") and OFFSET.

- Pattern and track edit features from FroeZe-X expander (copy, open, save as, clear, remove, SOLO and MUTE toggles,...).

- Sequencer playback requires an external clock source who provides **X32** BPM to work correctly. You can use KlokSpid clock module (free Ohmer Modules), *most used* Impromptu's CLOCKED/CKD module, or any well-working clock generator / multiplier / sequencer module.

- Time signature: 4/4 only, 16ths, 4 bars.

- Polyrhythm: not natively (due to 4/4 nature), but possible via euclidean from FroeZe-X expander (TRACK / EUCLID. page).

- Optional (from module's context menu): **internal QuadPercs sound engines!**, now QuadPercs sound engines are parts of FroeZe sequencer (for all instrument tracks). By this way, **FroeZe sequencer can delivers drum machines audio** (exactly like QuadPercs standalone module does), instead of 10ms triggers. This tricky feature may simplify patches who need drum machine sounds. Drum machine and its related drum kit can be immediately selected via left and right encoders. Proposed drum kits are always based on **instrument track nature** (only "kicks" for BD track, only snares for SD track, and so on). Some instrument tracks, such TB, may host many kind of kits (eg. TB track offers both timbales and tambourines, CB offers cowbells and bells, and so on).

- In case of main outputs send audio, FroeZe-X expander sends +10V gates (instead of 1ms triggers) on their related output jacks. Each gate is held while related drum kit sample is playing. This may be useful to control an external module (envelope generator, VCA, reverb/delay...)

- Pattern change can be controlled by triggers (previous, next), or by absolute pattern number via 0V ~ +10V control voltage (by enabling first "CV PATTERN" option, from module's context menu).

- Six models (GUI themes), identical than QuadPercs, KordZ, and some free modules from Ohmer Modules collection.

- All embedded displays are dimmable (luminous models), via left mouse click on "magic hotspot" (over the Ohmer logo, bottom-left side of FroeZe module) :slight_smile:. Please notice its linked FroeZe-X expander automatically adjusts as same model (GUI-theme) and same screen dim/bright setting!

----

Free version (without license key) is working as **full player** concerning **both trigger and audio engine QuadPercs modes** (all patterns/tracks are fully playable, even internal QuadPercs engine sounds, in order to keep the highest level of compatibility against shared patches created/edited by any *OhmerPrems member*). However, without license key and by using any patch made by *OhmerPrems member*, all controls & edit features are locked (every pattern/track/step) - except some allowed saving functions such patterns (any), QuadPercs-engine drum kits setting, and "8-slot" ratcheting setting (once per pattern).

When not using a configured FroeZe (from .vcv patch file) made by OhmerPrems member, after **Initialize** command (**Ctrl+I**, or **Command+I** on Mac), or on new FroeZe module instance, free version allows to edit **BD**, **SD** and **AC** tracks only, into the pattern 1 (all other patterns are edit-locked). Also, some edit features from FroeZe-X expander are inoperative (without any notification).

Free version: by using internal (QuadPercs) sounds (except in free player), allowed drum machines are strictly identical than standalone QuadPercs module: allowed drum machines are **Oberheim DMX**, **Drumulator**, **LinnDrum**, **Roland TR-707**, and **Roland TR-808**, at **44.1kHz only** (other drum machines and higher sample rates are reserved to OhmerPrems members exclusively). However, any drum machine (and higher sample rates than 44.1kHz) can be selected, but their sounds are muted (without any notification).
