# ![](doc/images/Logo_Ohmer.png)OhmerPrems (Premium modules)

*OhmerPrems* is both Premium (for susbcribers) and free plugin/modules, designed for VCV Rack 2.

Actually, *OhmerPrems* plugin is a set of two modules: **QuadPercs** , and (work-in-progress) **KordZ**.

**QuadPercs** module (all six liveries: Classic beige, Stage Repro, Absolute Night, Dark "Signature", Deepblue "Signature", Carbon "Signature"):

![](doc/images/QuadPercs_All_Models.png)(Notice the 4th module - _Absolute Night_ model, like 3rd, is bypassed: display, LED and backlight turned off!)

Some YouTube videos (made from old VCV Rack v0.6, but they're still valid), here:

[QuadPercs module presentation/tutorial from my YouTube channel "DoMiNo-MAO" (English, 1080p, 13 min.)](https://youtu.be/K51tFtwiisY) 

[Présentation/tutoriel du module QuadPercs sur ma chaîne YouTube "DoMiNo-MAO" (Français, 1080p, 13 mins.)](https://youtu.be/bAZPvrXWTXg)

[QuadPercs module in action, YouTube video made by Omar Brown (**thanks Omar!**)](https://www.youtube.com/watch?v=SBbM-12xc2w)

**KordZ** module (all six liveries - same than QuadPercs module), reduced room brightness:

![](doc/images/KordZ_All_Models.png)

[KordZ module in action (monophonic track) from Bitwig Studio 4 (uncommented, 1080p, 1'17")](https://www.youtube.com/watch?v=o6k0_MPDk3Y)

Modules by night: QuadPercs and KordZ modules are designed for VCV Rack's *Room brightness* feature (often named _Night mode_):

![](doc/images/QuadPercs_Dark_Room.png)(You can notice the *Absolute Night* model is the lone who have a yellow backligth dot-matrix display!)

"Signature"-line luxury models (Dark, Deepblue and Carbon) are using plasma-gas dot-matrix display (DMD), also visible by night. Concerning "Classic" and "Stage Repro" models, the display is LCD-based, without backlight (they're not visible by night).

Also, the KordZ modules by night (VCV Rack 2's *Room brightness* feature):

![](doc/images/KordZ_Dark_Room.png)

------

"***OhmerPrems***" subdirectory hosts either free/full version (built package is strictly identical), but without personal license key, all modules work as free version (with limitations, depending the module) . Full version requires a personal license key (the license key is sent by email during OhmerPrems subscription).

When installed, from VCV Rack module browser, QuadPercs and KordZ modules are listed (by brand, into "Ohmer Modules"). QuadPercs module is also listed as "Drum" and "Quad" categories when you're browsing by tags, KordZ module as "Visual" and "Polyphonic".

## HOW TO VERIFY YOUR PERSONAL LICENSE INSTALLATION?

Over **any OhmerPrems module**, just do a right-click mouse button to bring the context-menu. At the bottom of this menu, if the grayed entry indicates **License:** (followed by your partial license key), that meaning all your modules run as full version, as expected!

Otherwise, the same grayed menu entry indicates **Free**, followed by limitation type (between brackets).

![](doc/images/OhmerPrems_Free.png)

Hi! I'm enjoyed to present you my first *OhmerPrems* module: **QuadPercs**

Basically, QuadPercs is a 10HP **quad-channel drum** module, providing 4 independent drum machine channels, each having its own (sample-based) drum machine, and its related instrument.

QuadPercs module is available from OhmerPrems plugin, as both:

- free version (limited to **5** working drum machines) to any who want to try it (fully usable, no other limitation). Other drum machines can be selected, but are muted (no audio output).
- full version (all 16 drum machines), reserved to *OhmerPrems* members exclusively, requires a personal license key to remove all limitations.

Free version: Oberheim DMX, **Drumulator** (since Jan. 2023), LinnDrum, Roland 707, and Roland 808, for a total of 102 instruments.

Full version: Oberheim DMX, Drumulator, Korg KR-55, Korg Minipops, LinnDrum, Roland R8, Roland 606, Roland 626, Roland 707, Roland 808, Roland 909, Yamaha RX5, Yamaha RY-30, Casio RZ-1, Alesis SR-16, and E-MU XL-7, for a **total of 369 instruments!**

QuadPercs embeds all drum samples (44.1 kHz 16-bit mono FLAC, streamed from RAM for best performance), with anti-pop feature (to avoid weak noises when you're changing drum machine and/or its instrument on the fly).

KordZ module presentation coming soon...


------

## VERY IMPORTANT: QuadPercs operates correctly at 44.1 kHz

if **Engine sample rate** from VCV Rack is set to **another than 44.1 kHz**, the module will output **erratic/unrealistic sounds**!

I highly recommend to set the engine sample rate at 44.1 kHz while using QuadPercs module(s) in current rack. However, your output module (such **AUDIO-2**, **AUDIO-8**, or **AUDIO-16**) can be set to any sample rate you want (depending your audio interface capabilities), as long as Engine sample rate is set to 44.1 kHz.

------

## How to use QuadPercs

QuadPercs module is, in fact, very easy to use.

The main key are... four buttons (one per drum channel). Default channel is always 1.

For each channel (labeled 1 to 4, from top to bottom), you can find, from left to right:

- An ***input*** "TRIG." jack, to trigger drum sound for related channel. Minimum trigger voltage is +1.7V.
- Red LED, indicating selected channel (when lit), or when editing channel (while blinking).
- Small cyan segment-LED display above OUT jacks indicates the volume level for selected channel.
- Volume level (from 0% to 100%, default 50%) can be changed by turning the **rotary encoder**.
- Momentary button to select active channel (if its LED is off). When pressing button on **already active channel**, the LED turns blink, indicating channel edit. The related item to edit also blinks in dot-matrix display (DMD). When drum machine name is blinking, press the channel button (again) to change its instrument (drumkit). Turn the **rotary encoder** clockwise or counter-clockwise to select next or previous drum machine, or the instrument (drumkit) for current drum machine. No need to validate anything, your choice is *immediately applied!* Also, please notice while channel LED is blinking (meaning you're editing active channel), and in case you don't touch the rotary encoder nor any button, the edit mode ends - automatically - after 30 seconds (timeout).
- An ***output*** jack delivers monophonic audio, it can be connected to a mixer, effect, modulator input...

The dot-matrix display (DMD) reports the current selected channel (number indicated at top-left, channel LED does exactly the same thing), the current loaded drum machine for active (selected) channel, and its current instrument.

This module supports monophonic cables only (polyphony is never required for drum element).

Both *Initialize*, *Randomize* and *Preset* (via .vcvm preset file, or via copy/paste) commands, from module's context-menu (right-click, keyboard shortcuts), are fully supported.

------


## Free version

Free *OhmerPrems* plugin is available to everybody, for Windows, MacOS and Linux platforms, and can be downloaded directly from either [VCV Plugin Library](https://library.vcvrack.com/?query=&brand=Ohmer+Modules&tag=&license=) for automatic installation/updates, or via ["Releases"](https://github.com/DomiKamu/OhmerPrems/releases) page on this GitHub repository (but requires **manual** installation/updates, by download/copy **.vcvplugin** file).

------

## Full version (OhmerPrems members only)

Since VCV Rack 2, the plugin is EXACTLY the same than free version, except a personal license key is sent to OhmerPrems members (by email). The license key unlocks all modules to full (unrestricted) version.

Obviously, all *OhmerPrems* members will benefit all **lifetime** updates/upgrades and all future *OhmerPrems* modules (full versions) without any additional charge!

To become *OhmerPrems* member, simply send me **12 euros** (if required, please convert your local currency first, to fit with 12+ euros, otherwise your payment will not be accepted) via [my "PayPal.Me" (Dominique CAMUS @DominiqueCAMUS - BARJAC)](https://www.paypal.com/paypalme/DominiqueCAMUS).

Very important: don't forget to indicate:
- your first and last name.
- your valid email address (required to send your personal license key & instructions).
- also in the message, please specify **OhmerPrems member** (or something similar, to avoid possible confusion), thank you in advance.

New suscription requires from 24 to 48 hours after PayPal confirmation (in genereal, less than a day). **Incomplete fee informations or/and payment less than 10 euros is refurbished**. Thank you for your understanding.

------

## License Clauses

All ***OhmerPrems*** modules (even free) remain under **proprietary license**.

Full version is granted for each OhmerPrems member, and of course, **cannot be shared, sold or distributed** to any third party (obviously, the license key can be used on ALL owned computers). Please read "LICENSE-FULL.txt" enclosed in your downloaded package for licensing conditions.

All graphic materials, the "Ohmer" logo and related resources cannot be used for derivative works and remains the proprietary of Dominique Camus (Ohmer Modules & OhmerPrems developer).

All SVG graphics named **XB_*.svg** are designed by **Xavier Belmont** (ask him the permission if you'll want to use them in your developments). Thanks a lot, Xavier!

Thanks to **Marc Boulé** (author of excellent ImpromptuModular/Geodesics/MindMeld plugins) for C++ code who permit to swap ports textures (silver, gold) "on-the-fly" when changing model, exactly like momentary buttons and screws.

Thanks to **Paul Bacon** (author of excellent Bacon Music plugins, and working hard on SurgeXT) for C++ coding tips who permit to display coloured textures (Kordz's circle of fifths) in dark/night mode.

Thanks to **Steve Baker** and **Jens Peter Nielsen** for MacOS builds.

Feature requests, suggestions, and bug reports are welcome on this GitHub repository!
