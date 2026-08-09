# 6OP-DX USER'S MANUAL (UNDER CONSTRUCTION)

### TOPICS

- [**TERMINOLOGY**](#terminology)

_Factory Preset, preloaded Rom1a/Rom1b/Rom2a/Rom2b banks (4x32 voices), Aluminium model, DX7-emulated genuine LCD display:_
![](_img/main.png)

This will be the User's Manual for 6OP-DX module, **117HP** 6-operator algorithm-based FM (PM, phase modulation) synthesizer voice.

:warning: This manual will be built for future v2.6.14. **As draft at the moment!**

---

### TERMINOLOGY<a name="terminology"></a>

This topic explains some unfamiliar terms, most of them are used by Yamaha company for DX family synthesizers:

- **Voice** stands for synthesizer preset (or patch).
- **Bank** refers to internal memory, or a particular cartridge.
- **SysEx** stands for MIDI System Exclusive files (.syx), can host a full 32-voice bank, or a single voice.

---

The 6OP-DX offers 4 soundbanks, named **INT**, **CART1**, **CART2**, and **CART3**. Each bank holds 32 voices (a "voice" is a DX7 preset):
- **INT** (as internal memory). Every operator is using sine waveform only (like the real DX7 synthesizer).
- **CART1** (displayed **C1.**), as cartridge #1. Every operator is using sine waveform only (like the real DX7 synthesizer).
- **CART2** (displayed **C2.**), as cartridge #2. Every operator is using sine waveform only (like the real DX7 synthesizer).
- **CART3** (displayed **C3.**), as cartridge #3. Each operator may use custom waveform: sine (default), triangle, sawtooth, ramp, or square.

:warning: Due to DX7 compatibility, when you import a SysEx file to cartridge #3 (CART3/C3.), affected voices are automatically set to **sine** waveform for all operators.

---

When you bring a fresh 6OP-DX module in your rack (from module browser), or after **Initialize** command from right click menu (or via **Ctrl+I** / **Command+I** on MacOS X computers), the internal memory (INT) and all three cartridges (CART 1, CART2, and CART3) are empty: All banks are filled by 32 "INIT" voices.

However, by using VCV Rack 2's **Presets** feature, from right click menu, then **Factory Presets**, you'll can load prefilled ready-to-play banks (INT, C1/CART1, C2/CART2, and C3/CART3) with official Yamaha DX7 soundbanks (from official DX7 SysEx), respectively **Rom1a** (to **INT**ernal memory), **Rom1b** (to **CART**ridge 1), **Rom2a** (to **CART**ridge 2), and **Rom2b** (to **CART**ridge 3). This is useful in case you'd like to use 128 official DX7 voices/presets quickly, without sound design sessions, nor import operations!

:warning: By loading a proposed factory preset, please notice all banks of 32 voices are replaced by Rom1a, Rom1b, Rom2a, and Rom2b. So, don't forget to save your stuff prior to open a VCV Rack preset file!

By loading a proposed factory preset, the default selected voice is automatically set to **INT 11 E.PIANO 1** (the most used factory voice by numerous artists), as indicated by the DX7-emulated display. 

Proposed factory preset is using _Aluminium_ model (panel theme), with genuine DX LCD, like shown at the top of this manual. Of course, everything can be changed later, including model (panel theme) and DX7-emulated display (genuine LCD, backlit LCD retrofit, or OLED retrofit). You'll can assume this factory preset as a good start point for your project who are using 6OP-DX synth voice module.

![](_img/factorypresets.png)

---
