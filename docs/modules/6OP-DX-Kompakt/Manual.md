:warning:

Empty display, all LED always turned off, no extra right click menu, module is looking "dead" -> [**PLEASE CLICK HERE!**](https://github.com/DomiKamu/OhmerPrems/blob/v2/README.md) (top of page).

---

# 6OP-DX KOMPAKT USER'S MANUAL (UNDER CONSTRUCTION)

_The 6OP-DX Kompakt module, Aluminium model, DX7-emulated genuine LCD display:_
![](_img/main.png)

This will be the User's Manual for _6OP-DX Kompakt_ module, **34HP** 6-operator algorithm-based FM (PM, phase modulation) synthesizer voice, as "player".

:warning: This manual will be built for future v2.6.15. **As draft at the moment, and may change many times everyday!**

---

### TOPICS

- [**HISTORY**](#history)
- [**TERMINOLOGY**](#terminology)
- [**INTRODUCTION & FIRST WORDS**](#intro)
- [**TECHNICAL SPECIFICATIONS**](#techspecs)

---

### HISTORY<a name="history"></a>

_From English Wikipedia_: The DX7 is a synthesizer introduced by the Japanese Yamaha Corporation in 1983. It was the first successful digital synthesizer and is one of the best-selling synthesizers in history, selling more than 200,000 units.

_The Yamaha DX7 synthesizer_:
![](_img/theDX7synth.png)

Unlike other synthesizers prior the DX7, who are mostly analog synthesizers (using substractive synthesis), like the Minimoog (Moog Music), the MS-20 (Korg), the ARP 2600 (ARP Instruments), the Prophet 5 (Sequential Circuits), the Jupiter-8 (Roland), and many more, the Yamaha DX7 becomes the first affordable synthesizer using FM (Frequency Modulation) synthesis during 1983.

Frequency modulation (FM) synthesis was developed mainly by [John Chowning](https://en.wikipedia.org/wiki/John_Chowning) since 1967. The first synthesizer who have used the FM synthesis was the Synclavier, manufactured by New England Digital Corp.

In fact, the Yamaha DX7 is using a very close FM variant, named **PM** (**Phase Modulation**).

The DX7 synthesizer was used by many famous artists, like Phil Collins, Michael Jackson, Elton John, George Michael, Sade, A-ha, Prince, Tina Turner, Whitney Houston, Chicago, Billy Ocean, Harold Faltermeyer (Beverly Hills Cop theme, Top Gun Anthem), Genesis, Bon Jovi, Madonna, Stevie Wonder, Level 42, Queen, Berlin (Take My Breath Away), Brian Eno, and more!

The _6OP-DX Kompakt_ module for VCV Rack 2 will attempt to recreate - as closest as possible - the essence of the DX7 synthesizer (but without edit features, except **MONOPHONIC** state toggle, and modulation matrix), by using modernized technologies, in particular powerful CPUs, and improved sound quality offered by the most recent audio interfaces.

---

### TERMINOLOGY<a name="terminology"></a>

This topic explains some "unfamiliar" terms and accronyms. Most of them was used by Yamaha company for DX-family synthesizers:

- **Voice** stands for "synthesizer preset" (please do not confuse with VCV Rack 2 preset file).
- **Bank** may refer to internal memory or a specific cartridge, hosting 32 voices each.
- **SysEx** stands for MIDI System Exclusive files (.syx extension), can host a whole 32-voice bank (VMEM), or a single voice (VCED).
- **VMEM** is a particular DX7 SysEx _packed_ file format (defined by Yamaha) to store a whole 32-voice bank.
- **VCED** is a particular DX7 SysEx file format (defined by Yamaha) to store a single voice.
- **.6opsynth** is a proprietary binary file format used to store all synthesizer settings, including OP ON/OFF states and modulation matrices.
- **.6opcart** is a proprietary binary file format used to store a 32-voice cartridge/bank, including OP ON/OFF states and modulation matrices.

---

### INTRODUCTION & FIRST WORDS<a name="intro"></a>

Due to its reduced size (regardling its big brother, the _6OP-DX_ module), the _6OP-DX Kompakt_ module doesn't permit to do sound design, so voices cannot be edited. However, **MONOPHONIC** state (per voice) may be toggled on or off, and modulation matrix can be edited for any voice (including copy/paste feature between voices).

The best way is to open **.6opsynth** file (full synthesizer file), made by _6OP-DX_ module (who permit to edit sounds and modulation matrices). However, depending your needs, you'll can open a partial (cartridge-based) **.6opcart** file (this load the file in the currently selected bank, for 32 voices, including "extensions"), or import a DX7 SysEx file made by a real DX7 synthesizer, or compatible software (but without featured "extensions", such operator ON/OFF states and modulation matrices).

So you'll can consider:
- 6OP-DX (the huge module) either as voice synthesizer **AND** as voice (sound) editor, including modulation matrices (per voice).
- 6OP-DX Kompakt as "player", for final production in your racks, mainly to save space because 6OP-DX module is huge!

---

:information_source: Do not forget both _6OP-DX Kompakt_ and _6OP-DX_ modules are **free for everyone** (license V2 keyfile isn't required).

---

### TECHNICAL SPECIFICATIONS<a name="techspecs"></a>

- Designed to operate in VCV Rack 2 (v2.6.6, or higher), "Free" and "Pro" editions.
- Width: 34HP.
- Synthesis: Phase Modulation (PM), based on sine waveforms only (like the original DX synthesizer).
- Available models (panel themes): 8 (Aluminium, Stage Repro, Cobalt, Absolute Night, Dark "Signature", Fort Knox "Signature", Oxide "Signature", and Titanium "Signature").
- DX7-emulated display, may be genuine LCD, yellow-backlit LCD retrofit, or OLED retrofit (via right click menu).
- Emulated DX7 v1.8 firmware.
- 32 algorithms (all come from the real DX7 synthesizer), only for display.
- 6 operators.
- Polyphony: min. 1 channel/monophonic, max. 16 channels.
- Simplified panel to be operational for production.
- Large color OLED **touchscreen** display.
- Multipurpose continuous encoder (above the left-side of the touchscreen).
- MONOPHONIC toggle button, with purple LED (above the center of the touchscreen).
- Two multipurpose momentary buttons (above the right-side of the touchscreen).
- LFO waveforms: triangle, sawtooth (down), sawtooth up (ramp), square, sine, sample & hold.
- Input jacks: 16 (V/OCT, GATE, VELocity, AFTertouch, PB/pitch wheel, MW/modulation wheel, RETRIGger, VOICE, CV1 to CV8).
- Frequency response: from 27.5Hz (DX7 A-1 / international A0), to 8372.018Hz (DX7 C8 / international C9).
- Band-limiting: up to Nyquist frequency (half of sample rate).
- DAC resolution: 24-bit high-resolution DAC (original 12-bit DAC will be implemented later).
- Operational sample rate: recommended 44100Hz/48000Hz, or higher.
- Output jacks: 9 (MASTER output, OP1, OP2, OP3, OP4, OP5, OP6, P.EG, LFO).
- Output voltage ranges: -5V to +5V (10V peak-to-peak).
- Stereo: none (all outputs are mono).
- Polyphonic outputs: yes (up to 16 channels).
- Banks: 4 (named INT, CART1/C1, CART2/C2, CART3/C3), each holds 32 voices.
- Voices: 32 per bank (can be imported from VMEM SysEx file, or opened from **.6opcart** binary file with extended featurs).
- Individual voice can be imported from external VCED SysEx file.
- Full DX7 SysEx files support (either for VMEM 32-voice banks, and VCED single-voice): import only.
- Full 6OP-DX files support (**.6opsynth** for entire synthesizer, **.6opcart** for 32-voice cartridge, with extended features such modulation matrices and operator ON/OFF switch states - these features are not supported by DX7 SysEx).
- DX7 SysEx, **.6opcart** and **.6opsynth** files also can be imported/loaded by drag and drop (drop the file on the touchscreen).
- Bank/voice select by voltage: supported via discrete VOICE input jack (0V to +10V unipolar CV).
- 8 assignable independent CV input jacks.
- View DX7 settings for current voice (via 8 pages, by rotating the continuous encoder), access from MENU button.
- Modulation Matrix (via MENU button): each voice can use up to 16 customizable modulations.
- Modulation sources: 13 (VEL., AFT., MW, PB, CV1, CV2, CV3, CV4, CV5, CV6, CV7, CV8, LFO).
- Modulation targets: 90 (near all DX7 OP parameters, plus EG BIAS).
- Modulation ranges: -100% to +100% (RELative modulation), 0 to 100% (ABSolute modulation). Modulation can be inverted.
- Preferences (global preferences, via dedicated page, access from MENU button).
- "Keyboard" split & response range, adjustable from "Preferences".
- VCV Rack 2 Presets (.vcvm) support: Not supported (due to very huge amount of saved datas).
- VCV Rack 2 Modules Selections (.vcvs) support: Not supported (due to very huge amount of saved datas).
- Quick boot feature: on first installation in the rack, on full reset to factory (**Initialize** command, from right click menu).

---
---
---

## DRAFT

The 6OP-DX offers 4 banks, named **INT**, **CART1**, **CART2**, and **CART3**. Each bank hosts 32 voices:
- **INT** (as internal memory).
- **CART1** (displayed **C1.**).
- **CART2** (displayed **C2.**).
- **CART3** (displayed **C3.**).

---

When you bring a fresh 6OP-DX module in your rack (from module browser), or after **Initialize** command from right click menu, or via **Ctrl+I** keys shortcut (**Command+I** on MacOS X computers), the internal memory (INT) and all three cartridges (CART 1, CART2, and CART3) are filled by "INIT" voices.

However, you can download (and extract anywhere you'd like) two whole synthesizer binary files with prefilled banks (**.6opsynth** files).

First **.6opsynth** file is using respectively **Rom1a** (to **INT**ernal memory), **Rom1b** (to **CART**ridge 1), **Rom2a** (to **CART**ridge 2), and **Rom2b** (to **CART**ridge 3). Selected voice is BASS 1, as INT 1 (internal memory, voice number 1).

Second **.6opsynth** file is using respectively **Rom3a** (to **INT**ernal memory), **Rom3b** (to **CART**ridge 1), **Rom4a** (to **CART**ridge 2), and **Rom4b** (to **CART**ridge 3). Selected voice is FLUTE 1 (also as INT 1, the first voice of the bank).

All modulation matrices are empty.

You'll can assume these factory **.6opsynth** files can be a good start point for your projects who are using one or many 6OP-DX synth voice module(s), without effort.

:warning: **Due to very large amount of saved datas (approx. 28 kbytes for full synthesizer), both 6OP-DX / Kompakt modules don't support VCV Rack 2 Presets (.vcvm files) nor modules selections (.vcvs files).** Unfortunately it's due to VCV Rack 2 technical limitation.

---

:warning: Following DX7 parameters can't be modulated (they can't be selected as "target" from modulation matrix):

- OP SWITCH (operator on/off toggle).
- OP MODE (RATIO/FIXED toggle).
- OP EG levels (L1, L2, L3, and L4).
- OP BREAKPOINT (displayed "BREAK POINT=" in DX7-emulated LCD/OLED).
- OP L. CURVE potentiometer.
- OP R. CURVE potentiometer.
- LFO KEY SYNC toggle.
- OSC KEY SYNC toggle.
- LFO WAVEFORM selector.
- PITCH EG levels (L1, L2, L3, and L4).
- OUTPUT LEVEL potentiometer.
