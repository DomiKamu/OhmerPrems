# 6OP-DX USER'S MANUAL (UNDER CONSTRUCTION)

_Factory Preset, preloaded Rom1a/Rom1b/Rom2a/Rom2b banks (4x32 voices), Aluminium model, DX7-emulated genuine LCD display:_
![](_img/main.png)

This will be the User's Manual for 6OP-DX module, **117HP** 6-operator algorithm-based FM (PM, phase modulation) synthesizer voice.

:warning: This manual will be built for future v2.6.14. **As draft at the moment and change many times everyday!**

---

### TOPICS

- [**TERMINOLOGY**](#terminology)

---

### TERMINOLOGY<a name="terminology"></a>

This topic explains some "unfamiliar" terms and accronyms. Most of them was used by Yamaha company for DX-family synthesizers:

- **Voice** stands for synthesizer preset. Please do not confuse with VCV Rack 2 preset file!
- **Bank** may refer to internal memory, or a specific cartridge.
- **SysEx** stands for MIDI System Exclusive files (.syx extension), can host a whole 32-voice bank (VMEM), or a single voice (VCED).
- **VMEM** is a particular DX7 SysEx _packed_ file format (defined by Yamaha) to store a whole 32-voice bank.
- **VCED** is a particular DX7 SysEx file format (defined by Yamaha) to store a single voice.

---

The 6OP-DX offers four banks, named **INT**, **CART1**, **CART2**, and **CART3**. Each bank holds 32 voices:
- **INT** (as internal memory). Every operator is using sine waveform only (like the real DX7 synthesizer).
- **CART1** (displayed **C1.**), as cartridge #1. Every operator is using sine waveform only (like the real DX7 synthesizer).
- **CART2** (displayed **C2.**), as cartridge #2. Every operator is using sine waveform only (like the real DX7 synthesizer).
- **CART3** (displayed **C3.**), as cartridge #3. Each operator may use custom waveform: sine (default), triangle, sawtooth, ramp, or square.

:warning: Due to DX7 compatibility, when you import a SysEx file to cartridge #3 (CART3/C3.), affected voice(s) is/are automatically set to **sine** waveform, for all 6 operators.

---

When you bring a fresh 6OP-DX module in your rack (from module browser), or after **Initialize** command from right click menu, or via **Ctrl+I** keys shortcut (**Command+I** on MacOS X computers), the internal memory (INT) and all three cartridges (CART 1, CART2, and CART3) are filled by (32) "INIT" voices.

However, from right click menu, by using VCV Rack 2's **Presets**, then **Factory Presets**, you'll can load prefilled ready-to-play banks (INT, C1/CART1, C2/CART2, and C3/CART3) with official Yamaha DX7 soundbanks (SysEx files), respectively **Rom1a** (to **INT**ernal memory), **Rom1b** (to **CART**ridge 1), **Rom2a** (to **CART**ridge 2), and **Rom2b** (to **CART**ridge 3). This is useful in case you'd like to use 128 official DX7 voices quickly, without sound design sessions, nor file operations!

:warning: By loading the proposed factory preset, please notice all banks of 32 voices are replaced by Rom1a, Rom1b, Rom2a, and Rom2b. So, don't forget to save your stuff prior to open a VCV Rack preset file!

By loading the proposed factory preset, the default selected voice is automatically switched to **INT 11 E.PIANO 1** (it's the most used factory voice by numerous artists), as indicated by the DX7-emulated display. 

The proposed factory preset is using _Aluminium_ model (panel theme), and genuine DX LCD, exactly like shown at the top of this manual. Of course, everything can be changed later, including model (panel theme) and DX7-emulated display (genuine LCD, yellow-backlit LCD retrofit, or OLED retrofit). You'll can assume this factory preset as a good start point for your projects who are using one or many 6OP-DX synth voice module(s).

![](_img/factorypresets.png)

---
