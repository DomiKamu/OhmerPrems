**BE CAREFUL - CAUTION - ATTENTION:** New subscriptions are postponed to November 1st, 2018 (apologizes for this delay, for npw I'm away from my development computer). Actually any PayPal are refund.

# ![](doc/images/Logo_Ohmer.png)OhmerPrems (Premium module + free)

*OhmerPrems* is both Premium (for suscribers) and free plugin/modules, designed for VCV Rack v0.6.

Actually *OhmerPrems* plugin is containing **QuadPercs** module. A bigger model is in "designing" phase...

![QuadPercs - All models](./doc/images/QPCS_all_models.png)



Some YouTube videos, here:

[QuadPercs module presentation/tutorial from my YouTube channel (English, 1080p, 13 min.)](https://youtu.be/7e7qjuJyDj0) 

[Présentation/tutoriel du module QuadPercs sur ma chaîne YouTube (Français, 1080p, 13 mins.)](https://youtu.be/jkP7m8JSPrk)

[QuadPercs module in action, YouTube video made by Omar Brown (Thanks!)](https://www.youtube.com/watch?v=SBbM-12xc2w)

[QuadPercs modules in action, YouTube video made by Billy Sorel (Thanks mon Ami!)](https://www.youtube.com/watch?v=-_YcB-VNbCE)



------

###### IMPORTANT - ABOUT INSTALLATION: from your "***documents/Rack/plugins***" directory, if existing, never touch "***Ohmer***" subdirectory (in case you're already using regular "Ohmer Modules", like KlokSpid, Metriks, RKD, etc), so please understand "***OhmerPrems***" is a SEPARATE plugin and never replace (or merge) with existing "***Ohmer***", anyway! PLEASE ALWAYS USE DIRECTORY NAMES PROVIDED FROM RESPECTIVE DOWNLOADED .ZIP FILES TO AVOID ISSUES!

"***OhmerPrems***" subdirectory hosts either free or full version (simply delete existing "OhmerPrems" directory first, then replace it by provided from downloaded full version .zip archive file, for OhmerPrems members).

When installed, from Rack's browser, QuadPercs module is listed from "Ohmer Modules". QuadPercs module is also listed from "Drum" and "Quad" when you're browsing by tags.

------

Hi! I'm enjoyed to present you my first *OhmerPrems* module: **QuadPercs**

Basically, QuadPercs is a 10 HP **quad-channel drum** module, providing 4 independent drum/percussion channels, each having its own (sample-based) drum machine, and its related instrument.

QuadPercs module is available from OhmerPrems plugin, as both:

- free version (limited to 4 drum machines) to any who want to try it (fully usable, no other limitation).
- full version, reserved to *OhmerPrems* members.

Free version: Oberheim DMX, LinnDrum, Roland 707, and Roland 808 (for a total of 90 instruments).

Full version: Oberheim DMX, Drumulator, Korg KR-55, Korg Minipops, LinnDrum, Roland R8, Roland 606, Roland 626, Roland 707, Roland 808, Roland 909, Yamaha RX5, Yamaha RY-30, Casio RZ-1, Alesis SR-16, and E-MU XL-7, for a **total of 369 instruments!**

QuadPercs embeds all drum samples (44.1 kHz 16-bit mono, streamed from RAM for best performance), with anti-pop feature (to avoid bad noised when you're changing drum machine and/or its instrument). Like KlokSpid and Metriks modules (provided from Ohmer Modules), QuadPercs is available as six models, shown by screen capture, top of this document, can be changed via right-click (context) menu.

**VERY IMPORTANT: QuadPercs operates at 44100Hz only!** if Rack engine is set to another sample rate, the module is automatically disabled: all channel LEDs are turned on, and its dot-matrix display indicates "44100Hz", because internal samples are 44100Hz only (no internal re-sampling yet). Changing Rack's sample rate to 44100Hz will return QuadPercs module(s) as operational.

QuadPercs is very easy to use. The main key are... four buttons (one per channel). Default channel is always 4.
For each channel, labeled 1 to 4, you can find from left to right:

- An ***input*** "TRIG." jack, to trigger drum sound for related channel. Minimum trigger voltage is +1.7V.
- Red LED, indicating currently selected channel (when lit), or when editing channel (while blinking).
- Momentary button to select active channel (if its LED is off). When pressing button on **already active channel**, the LED blinks, indicating channel edit. The related item to edit also blink in dot-matrix display (DMD). When drum machine name is blinking, press the channel button (again) to change its instrument. Turn the **rotary encoder** clockwise or counter-clockwise to select next / previous drum machine, or its instrument. No need to validate anything, your choice is *immediately applied!* Also, please notice while channel LED is blinking (meaning you're editing active channel), if you don't touch the rotary encoder nor any button, the edit mode ends - automatically - after 30 seconds (it's a kind of timeout). **Rotary encoder doesn't have effect while LED doesn't blink**, to avoid unwanted changes.
- An ***output*** jack (monophonic sound) can be connected to a mixer, effect, modulator input, etc.

The dot-matrix display (DMD) reports the current selected channel (number indicated at top-left, channel LED does exactly the same thing), the current loaded drum machine for active (selected) channel, and its current instrument.




## Free version

Free *OhmerPrems* plugin is available to everybody, for Windows, MacOS and Linux platforms, and can be downloaded directly from ["Releases"](https://github.com/DomiKamu/OhmerPrems/releases) page on this GitHub repository. This plugin isn't available from "VCV Plugins" website and, by this way, cannot be installed via Rack's Plugin Manager.



## Full version (OhmerPrems members only)

Full version of OhmerPrems plugin (modules) is accessible only for *OhmerPrems* members (download link pointing to full personal version is **always** sent by email, including future updates).

The registration fee to become *OhmerPrems* member is **8 €**, via [PayPal](https://www.paypal.me/DominiqueCAMUS) only. For other currencies, please do a *conversion to euro/EUR* first. Delivery delay to OhmerPrems members is less than 24 hours (2 to 6 hours, in general). Indicated price may change, depending stuff behind OhmerPrems plugin/modules (of course, this doesn't concern previously registered OhmerPrems members!).

Obviously all *OhmerPrems* members will benefit all **lifetime** updates/upgrades and all future *OhmerPrems* modules (in full versions), without any additional charge!

**To OhmerPrems members**: be careful in case you'll share your patches (.vcv files) on patchstorage (or equivalent) website, by using drum machine(s) provided in full version of QuadPercs, please keep in mind all users don't have the full version, too, and in this case, channels using drum machines included in full version will return automatically to default "Oberh. DMX Kick 1"! Thanks in advance to consider it.



## License Clauses

All ***OhmerPrems*** modules (even free) remain under **proprietary license**.
Full version is watermaked for each member, and of course, cannot be shared, sold or distributed to any third party (obviously, it can be used on all owned computers). Please read "LICENSE.txt" enclosed in your downloaded package.
All graphic materials, Ohmer logo and related resources cannot be used for derivative works and remains the proprietary of Dominique Camus (Ohmer Modules & OhmerPrems developer).



Feature requests, suggestions, and bug reports are welcome on this GitHub repository.
