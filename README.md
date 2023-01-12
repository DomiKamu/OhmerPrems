# ![](doc/images/Logo_Ohmer.png)OhmerPrems (Premium modules)

*OhmerPrems* is both Premium (for susbcribers) and free plugin/modules, designed for VCV Rack 2.

Actually, *OhmerPrems* plugin is containing two modules: **QuadPercs** , and (work-in-progress) **KordZ**. More modules are under consideration.

**QuadPercs** module (all six models):

![](doc/images/QuadPercs_All_Models.png)

Some YouTube videos (made from old VCV Rack v0.6, but they're still valid), here:

[QuadPercs module presentation/tutorial from my YouTube channel "DoMiNo-MAO" (English, 1080p, 13 min.)](https://youtu.be/K51tFtwiisY) 

[Présentation/tutoriel du module QuadPercs sur ma chaîne YouTube "DoMiNo-MAO" (Français, 1080p, 13 mins.)](https://youtu.be/bAZPvrXWTXg)

[QuadPercs module in action, YouTube video made by Omar Brown (**thanks Omar!**)](https://www.youtube.com/watch?v=SBbM-12xc2w)

**KordZ** module (all six models):

![](doc/images/KordZ_All_Models.png)

[KordZ module in action (monophonic track) from Bitwig Studio 4 (uncommented, 1080p, 1'17")](https://www.youtube.com/watch?v=o6k0_MPDk3Y)

------

"***OhmerPrems***" subdirectory hosts either free/full version (built package is strictly identical), but without personal license key, all modules work as free version (with limitations, depending the module) . Full version requires a personal license key (the license key is sent by email during OhmerPrems subscription).

When installed, from VCV Rack module browser, QuadPercs and KordZ modules are listed (by brand, into "Ohmer Modules"). QuadPercs module is also listed as "Drum" and "Quad" categories when you're browsing by tags, KordZ module as "Visual" and "Polyphonic".

## HOW TO VERIFY YOUR PERSONAL LICENSE INSTALLATION?

Over **any OhmerPrems module**, just do a right-click mouse button to bring the context-menu. At the bottom of this menu, if the grayed entry indicates **License:** (followed by your partial license key), that meaning all your modules run as full version, as expected!

Otherwise, the same grayed menu entry indicates **Free**, followed by limitation type (between brackets).

![](doc/images/OhmerPrems_Free.png)

------
FROM THIS POINT, THIS DOCUMENT WILL BE ENHANCED (WORK IN PROGRESS)

------

Hi! I'm enjoyed to present you my first *OhmerPrems* module: **QuadPercs**

Basically, QuadPercs is a 10HP **quad-channel drum** module, providing 4 independent drum machine channels, each having its own (sample-based) drum machine, and its related instrument.

QuadPercs module is available from OhmerPrems plugin, as both:

- free version (limited to **5** working drum machines) to any who want to try it (fully usable, no other limitation). Other drum machines can be selected, but are muted (no audio output).
- full version (all 16 drum machines), reserved to *OhmerPrems* members exclusively, requires a personal license key to remove all limitations.

Free version: Oberheim DMX, **Drumulator** (since Jan. 2023), LinnDrum, Roland 707, and Roland 808, for a total of 102 instruments.

Full version: Oberheim DMX, Drumulator, Korg KR-55, Korg Minipops, LinnDrum, Roland R8, Roland 606, Roland 626, Roland 707, Roland 808, Roland 909, Yamaha RX5, Yamaha RY-30, Casio RZ-1, Alesis SR-16, and E-MU XL-7, for a **total of 369 instruments!**

QuadPercs embeds all drum samples (44.1 kHz 16-bit mono FLAC, streamed from RAM for best performance), with anti-pop feature (to avoid weak noises when you're changing drum machine and/or its instrument on the fly).




------

## VERY IMPORTANT: QuadPercs operates at 44.1 kHz ONLY!

if VCV Rack Engine's sample rate is set to **another than 44.1 kHz**, the module becomes _"inop."_ (inoperative) immediately: in this case, all channel LEDs blink fast, the upper line on display indicates **!!MODULE INOP.!!** (as fast blinking message), and instructions are given on the second line of display.

![](doc/images/Sample_Rate_44100_Message.png)

This limitation is, for now, mandatory, to avoid... unrealistic drumkit sounds!

To operate properly at higher sample rates, internal resampling (+ filtering/FIR) algorithm must be efficiently implemented. **This feature remains under investigation**. 

Changing VCV Rack Engine's sample rate back to 44.1 kHz will return QuadPercs module(s) as operational, immediately. However, your output module (such VCV Core AUDIO-2, AUDIO-8, or AUDIO-16) can be set to any sample rate (QuadPercs modules in your rack aren't affected).

------

## How to use QuadPercs

QuadPercs module is, in fact, very easy to use.

The main key are... four buttons (one per drum channel). Default channel is always 1.

For each channel (labeled 1 to 4, from top to bottom), you can find, from left to right:

- An ***input*** "TRIG." jack, to trigger drum sound for related channel. Minimum trigger voltage is +1.7V.
- Red LED, indicating currently selected channel (when lit), or when editing channel (while blinking).
- Momentary button to select active channel (if its LED is off). When pressing button on **already active channel**, the LED turns blink, indicating channel edit. The related item to edit also blinks in dot-matrix display (DMD). When drum machine name is blinking, press the channel button (again) to change its instrument (drumkit). Turn the **rotary encoder** clockwise or counter-clockwise to select next or previous drum machine, or the instrument (drumkit) for current drum machine. No need to validate anything, your choice is *immediately applied!* Also, please notice while channel LED is blinking (meaning you're editing active channel), and in case you don't touch the rotary encoder nor any button, the edit mode ends - automatically - after 30 seconds (timeout). **Rotary encoder doesn't have effect while LED doesn't blink**, in order to avoid unwanted changes.
- An ***output*** jack (delivers monophonic audio sound) can be connected to a mixer, effect, modulator input...

The dot-matrix display (DMD) reports the current selected channel (number indicated at top-left, channel LED does exactly the same thing), the current loaded drum machine for active (selected) channel, and its current instrument.

This module supports monophonic cables only (polyphony is never required for drum element).

Both *Initialize*, *Randomize* and *Preset* (via .vcvm preset file, or via copy/paste) commands, from module's context-menu (right-click, keyboard shortcuts), are fully supported.

------


## Free version

Free *OhmerPrems* plugin is available to everybody, for Windows, MacOS and Linux platforms, and can be downloaded directly from either [VCV Plugin Library](https://library.vcvrack.com/?query=&brand=Ohmer+Modules&tag=&license=) for automatic installation/updates, or via ["Releases"](https://github.com/DomiKamu/OhmerPrems/releases) page on this GitHub repository (but requires **manual** installation/updates, by copying downloaded **.vcvplugin** file).

------

## Full version (OhmerPrems members only)

Since VCV Rack 2, the plugin is the same than free version, except a personal license key is sent to OhmerPrems members, by email. The personal license key unlocks all modules to full version.

Obviously, all *OhmerPrems* members will benefit all **lifetime** updates/upgrades and all future *OhmerPrems* modules (full versions) without any additional charge!

To become *OhmerPrems* member, simply send me **10 euros** (if required, please convert your local currency first, to fit with 10+ euros, otherwise your payment will be refunded) via [my Paypal.Me (Dominique CAMUS @DominiqueCAMUS - BARJAC)](https://www.paypal.com/paypalme/DominiqueCAMUS).

Don't forget to indicate:
- your first & last name.
- your valid email address.
- in the free message, please specify **OhmerPrems** or something similar.

New suscription requires from 24 to 48 hours after PayPal confirmation.

------

## License Clauses

All ***OhmerPrems*** modules (even free) remain under **proprietary license**.

Full version is granted for each member, and of course, **cannot be shared, sold or distributed** to any third party (obviously, the license key can be used on ALL owned computers). Please read "LICENSE-FULL.txt" enclosed in your downloaded package for licensing conditions.

All graphic materials, Ohmer logo and related resources cannot be used for derivative works and remains the proprietary of Dominique Camus (Ohmer & OhmerPrems developer).

All SVG graphics named **XB_*.svg** are designed by **Xavier Belmont** (ask him the permission if you'll want to use them in your developments). Thanks a lot, Xavier!

Thanks to **Marc Boulé** (author of excellent ImpromptuModular/Geodesics/MindMeld plugins) for C++ code who permit to swap ports textures (silver, gold) "on-the-fly" when changing model, exactly like momentary buttons and screws.

Thanks to **Steve Baker** and **Jens Peter Nielsen** for MacOS builds.

Feature requests, suggestions, and bug reports are welcome on this GitHub repository!
