**VCV RACK v1:** OhmerPrems plugin v1.0.2 (for now, QuadPercs module) is available for VCV Rack **v1.x.x** (Windows, Mac and Linux). Full version for each OhmerPrems member is also available (please see your mailbox). Free version (only) is available for all platforms either from [VCV Plugin Library](https://vcvrack.com/plugins.html#Ohmer) or "Releases" on this GitHub repository (downloads from _lastest release_).



# ![](doc/images/Logo_Ohmer.png)OhmerPrems (Premium module + free)

*OhmerPrems* is both Premium (for susbcribers) and free plugin/modules, designed for VCV Rack v1.

Actually *OhmerPrems* plugin is containing **QuadPercs** module only. More modules are under consideration.

![](doc/images/QuadPercs_All_Models.png)
_(please note this image comes from OhmerPrems v1.0.2, VCV Rack v1.0.0 Windows)_

Some YouTube videos (was made from VCV Rack v0.6 but still valid). **English and French "tutos" was updated to VCV Rack v1.1.0 (July 1st, 2019)**:

[QuadPercs module (v1) tutorial from my YouTube channel "DoMiNo-MAO" (English, 29 min.)](https://youtu.be/K51tFtwiisY) 

[Tutoriel du module QuadPercs (v1) sur ma chaîne YouTube "DoMiNo-MAO" (Français/French, 30 mins.)](https://youtu.be/bAZPvrXWTXg)

[QuadPercs module in action (VCV Rack 0.6, 2018), YouTube video made by **Omar Brown** (thanks!)](https://www.youtube.com/watch?v=SBbM-12xc2w)

[QuadPercs modules in action (VCV Rack v0.6, 2018), YouTube video made by **Billy Sorel** (merci !)](https://www.youtube.com/watch?v=-_YcB-VNbCE)

------

###### ABOUT INSTALLATION: from your "***documents/Rack/plugins-v1***" directory, if existing, never touch "***Ohmer***" folder (in case you're already using regular "Ohmer Modules", like KlokSpid, Metriks, RKD, Splitter 1x9 etc), so please understand "***OhmerPrems***" is a SEPARATE plugin and never replace (or merge) with existing other folder, anyway! PLEASE ALWAYS USE DIRECTORY NAMES PROVIDED FROM RESPECTIVE DOWNLOADED .ZIP FILES TO AVOID ISSUES/CONFICTS!

"***OhmerPrems***" subdirectory hosts either free or full version (simply delete existing "OhmerPrems" directory first, then replace it by provided from downloaded full version .zip archive file, for OhmerPrems members). Free version plugin.dll/plugin.so/plugin.dylib is smaller than full version equivalent, because unavailable samples (for disabled drum machines) aren't implemented.

When installed, from Rack's browser, QuadPercs module is listed by Brands into "Ohmer Modules". QuadPercs module is also listed as "Drum" and/or "Quad" categories when you're browsing by tags.

Obviously, you can use both OhmerPrems plugin (either Full **OR** Free - *OhmerPrems* folder) and Ohmer Modules plugin (*Ohmer* folder) together!

------

Hi! I'm enjoyed to present you my first *OhmerPrems* module: **QuadPercs**

Basically, QuadPercs is a 10 HP **quad-channel drum/percussion** module, providing 4 independent drum/percussion channels, each having its own (sample-based) drum machine, and its related instrument (aka drumkit).

QuadPercs module is available from OhmerPrems plugin, as both:

- free version (limited to 4 drum machines) to any who want to try it (fully usable, no other limitation).
- full version (all 16 drum machines), reserved to *OhmerPrems* members only.

Free version: Oberheim DMX, LinnDrum, Roland 707, and Roland 808 (for a total of 90 instruments).

Full version: Oberheim DMX, Drumulator, Korg KR-55, Korg Minipops, LinnDrum, Roland R8, Roland 606, Roland 626, Roland 707, Roland 808, Roland 909, Yamaha RX5, Yamaha RY-30, Casio RZ-1, Alesis SR-16, and E-MU XL-7, for a **total of 369 instruments!**

QuadPercs embeds all drum samples (44.1 kHz 16-bit mono, streamed from RAM for best performance), with anti-pop feature (to avoid weak noises when you're changing drum machine and/or its instrument on the fly). Like KlokSpid module (provided from Ohmer Modules), QuadPercs is available as six models, shown by screen capture, top of this document, model can be changed via right-click (context) menu.

------

## VERY IMPORTANT: QuadPercs operates at 44.1 kHz ONLY!

if VCV Rack Engine's sample rate is set to **another than 44.1 kHz**, the module becomes _"inop."_ (inoperative) immediately: in this case, all channel LEDs blink fast, the upper line on display indicates **!!MODULE INOP.!!** (module inoperative) as fast blinking message, and instructions are given on the second line of the DMD!

![](doc/images/Sample_Rate_44100_Message.png)

This limitation is, for now, mandatory, to avoid... unrealistic drumkit sounds (played too quickly)!

Changing VCV Rack Engine's sample rate back to 44.1 kHz will return QuadPercs module(s) as operational, immediately.

However, output module (**AUDIO-8** or **AUDIO-16**, from Core) can be set to any sample rate, depending your output (audio interface, bridge to DAW) can support. In this case, QuadPercs module works normally.

------

## How to use QuadPercs

QuadPercs module is, in fact, very easy to use.

The main key are... four buttons (one per drum channel). Default channel is always 1.

For each channel (labeled 1 to 4, from top to bottom), you can find, from left to right:

- An ***input*** "TRIG." jack, to trigger drum sound for related channel. Minimum trigger voltage is +1.7V.
- Red LED, indicating currently selected channel (when lit), or when editing channel (while blinking).
- Momentary button to select active channel (if its LED is off). When pressing button on **already active channel**, the LED turns blink, indicating channel edit. The related item to edit also blinks in dot-matrix display (DMD). When drum machine name is blinking, press the channel button (again) to change its instrument (drumkit). Turn the **rotary encoder** clockwise or counter-clockwise to select next or previous drum machine, or the instrument (drumkit) for current drum machine. No need to validate anything, your choice is *immediately applied!* Also, please notice while channel LED is blinking (meaning you're editing active channel), and in case you don't touch the rotary encoder nor any button, the edit mode ends - automatically - after 30 seconds (timeout). **Rotary encoder doesn't have effect while LED doesn't blink**, in order to avoid unwanted changes.
- An ***output*** jack (delivers monophonic sound) can be connected to a mixer, effect, modulator input...

The dot-matrix display (DMD) reports the current selected channel (number indicated at top-left, channel LED does exactly the same thing), the current loaded drum machine for active (selected) channel, and its current instrument.

This module supports monophonic cables only.

Since OhmerPrems v1.0.2, both *Initialize*, *Randomize* and *Preset* (via copy/paste, or .vcvm module preset file) commands, from module's context-menu (right-click, keyboard shortcuts), are fully supported!

------


## Free version

Free *OhmerPrems* plugin is available to everybody, for Windows, MacOS and Linux platforms, and can be downloaded directly from either [VCV Plugin Library](https://vcvrack.com/plugins.html#ohmer) for automatic installation/updates, or via ["Releases"](https://github.com/DomiKamu/OhmerPrems/releases) page on this GitHub repository (but requires **manual** installation and updates).

**CAUTION: this is free version, by the way it's not applicable for OhmerPrems members!**

------

## Full version (OhmerPrems members only)

Full version of OhmerPrems plugin (modules) is accessible only for *OhmerPrems* members (download link pointing to full personal version is **always** sent by email, including future updates).

The registration fee to become *OhmerPrems* member is now **10 EUR**, via [PayPal](https://www.paypal.me/DominiqueCAMUS) only. For other currencies, please do a *conversion to euro/EUR* first. Delivery delay to OhmerPrems members is less than 24 hours (2 to 6 hours, in general).

Obviously all *OhmerPrems* members will benefit all **lifetime** updates/upgrades and all future *OhmerPrems* modules (full versions), without any additional charge!

**To OhmerPrems members**: be careful in case you'll share your patches (.vcv files) on patchstorage (or equivalent) website, by using drum machine(s) provided in full version of QuadPercs, please keep in mind all users don't have the full version, too, and in this case, channels using drum machines included in full version (but not in free) will return automatically to default "Oberh. DMX Kick 1"! So, thanks in advance to consider it!

------

## License Clauses

All ***OhmerPrems*** modules (even free) remain under **proprietary license**.

Full version is watermaked for each member, and of course, cannot be shared, sold or distributed to any third party (obviously, it can be used on all owned computers). Please read "LICENSE-FULL.txt" enclosed in your downloaded package.

All graphic materials, Ohmer logo and related resources cannot be used for derivative works and remains the proprietary of Dominique Camus (Ohmer Modules & OhmerPrems developer).

All SVG graphics named **XB_*.svg** are designed by **Xavier Belmont** (ask him the permission if you'll want to use them in your productions). Thanks a lot, Xavier!

Thanks to **Marc Boulé** (author of excellent ImpromptuModular/Geodesics plugins) for C++ code who permit to swap ports textures (silver, gold) "on-the-fly" when changing model, exactly like momentary buttons and screws.

Feature requests, suggestions, and bug reports are welcome on this GitHub repository.
