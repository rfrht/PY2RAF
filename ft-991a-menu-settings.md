# FT-991/A Main Menu Settings
I have found that the transceiver manual is um... Less than friendly, let's say.

This intends to be an easy-to-understand with a practical focus on 991/A menu and functionalities.

See also: [FT-991/A Articles, hints, tips and tricks](https://github.com/rfrht/FT-991A/wiki)

## Table of Contents

| The menu items are grouped | In approximate function groups |
| --- | --- |
| [Page 1 - Front-End signal treatment](#page-1) | [Page 2 - Digital Signal Processing and filtering](#page-2) |
| [Page 3 - Miscellaneous](#page-3) | [Page 4 - CW Functions](#page-4) |
| [Page 5 - Power & Gain Settings](#page-5) | [Page 6 - Ancillary Tuning options](#page-6) |
| [Page 7 - FM Functions](#page-7) | [Page 8 - C4FM and Encoding functions](#page-8) |
| [Page 9 - Pre-recorded playback messages](#page-9) | [Page 10 - Bottom Row Configuration Menu](#page-10) |

***

# Page 1
Front-End signal treatment

| [NAR/WIDE](#narwide) | [NB](#nb) | [AGC](#agc) | [5/10Hz](#510-hz) |
| --- | --- | --- | --- |
| [<= BACK](#page-10) | **[ATT](#att)** | **[IPO](#ipo)** | [FWD =>](#page-2) |

## NAR/WIDE
* **WHAT:** This toggles your transceiver receiving front-end width, from narrow or wide.
* **AVAILABLE OPTIONS:** W (wide) or N (narrow)
* **RX or TX?** All modes: RX; except FM which affects both TX and RX.
* **WHICH MODE?** All modes except C4FM
* **WHEN TO USE** While the *Wide* (W) will be more comfortable for listening for signals, there may be times where you have a strong neighbouring throwing some signal in your passband. Move it to *Narrow* (N), so you can (try to) escape the interfering signal. Also, if you are DXing, you might want to use an narrower bandwidth, because with narrower signal, you also get less noise to cope with. The *Narrow* mode is also useful in digital modes and FT8, so you can dodge that nearby QRO station attacking your AGC - Learn more in [this article](/rfrht/FT-991A/wiki/Using-FT-991A-Filters-to-Improve-your-FT-8-Reception). *Narrow* can be useful in Contests or busy bands to filter out nearby interfering signals, and occupying less spectrum.
* **CAVEAT:** Use this setting in tandem with the [WIDTH](#width) function, so if you are using phone modes the narrow audio won't be too... Narrow. Also, if you are doing SSB and the audio reception might sound too tight, you might have unintentionally entered the "N" mode. Switch back to "W" mode. In FM mode, the `NAR/WIDE` **also** affects the TX bandwidth.

## NB
* **WHAT:** This is the noise blanker. What is a noise blanker? It is a filter that wipes out quick spikes/impulse noise, like electric fence clicking, car ignition, brushed motors
* **AVAILABLE OPTIONS:** On or Off.
* **RX or TX?** RX
* **WHICH MODE?** All except FM & C4FM
* **WHEN TO USE:** If you hear some repetitive clicking, give NB a go!
* **CAVEAT:** This is also useful in SSB digital modes. And do not mistake with [DNR](#dnr).

## AGC
* **WHAT:** This is the Automatic Gain Control. Seriously, what's that? The AGC controls the gain (doh) of the receiving stage of your equipment. Let an example, you are having an contact with that hard to copy station and then all of sudden, you get some S9+ static crash - the signal goes away and takes some time so you can hear the station again. That's the AGC slowly recovering from the spike, gradually increasing the gain until it get to the signal. That's the `Slow` behaviour. Now, if your AGC is set to `Fast`, the AGC recovers way faster and you will get to the signal in a shorter time. However, the `Fast` tends to be uncomfortable in SSB phone when the participants have fair or better signal, getting back to the noise floor quickly and making noisier speech pauses/silence.
* **AVAILABLE OPTIONS:** Auto, Fast, Mid, Slow.
* **RX or TX?** RX
* **WHICH MODE?** CW, SSB, AM
* **WHEN TO USE:** If doing phone, leave it in `Auto` or `Slow` - Unless you are doing DX or hard to copy station, then the `Fast` is a must.
* **CAVEAT:** The default `Auto` setting will define Fast for Digital / CW and `Slow` for SSB.

## 5/10 Hz
* **WHAT:** This is the Clarifier minimum adjustment step.
* **AVAILABLE OPTIONS:** 10 Hz, 5 Hz
* **RX or TX?** RX
* **WHICH MODE?** SSB and CW.
* **WHEN TO USE:** If you have golden ears, use 5 Hz steps. Otherwise 10 Hz is ought be good nuff for ya.
* **CAVEAT:** --

## ATT
* **WHAT:** This function enables the Attenuator. Reduces the receiving signal by 4 S-units in the meter (-12 dB).
* **AVAILABLE OPTIONS:** On, Off
* **RX or TX?** RX
* **WHICH MODE?** All modes, however only in HF-6m. Not available in 144 or UHF.
* **WHEN TO USE:** It is useful to defend from a very strong signal, potentially overloading your front-end. In the manual, there's a caveat stating that the Attenuator is also useful if you have more than 3 S-units of fluctuation in your noise floor (QRN, etc.) - that's actually a good trick! Otherwise, you will want the attenuator to `Off`.
* **CAVEAT:** If you need to attenuate a signal, ensure that you don't have any preamplifier active - Ensure that the [IPO](#ipo) function is in the `IPO` setting. If you see the `AMP1` or `AMP2` marking in display, move it back to `IPO` first. Doesn't make much sense to attenuate what you are amplifying beforehand...

## IPO
* **WHAT:** That's an horrid and counter-intuitive name for an very common feature: Signal Amplifier.
* **AVAILABLE OPTIONS:** IPO (Amplifier off), AMP1 (Almost quadruplicates the signal, +10 dB gain), AMP2 (Almost 7-fold amplification of a signal, +20 dB gain)
* **RX or TX?** RX
* **WHICH MODE?** All modes, but HF-6m only. Not available in 144 or UHF.
* **WHEN TO USE:** Do you have a **noise floor** (noise floor: The amount of signal you get in idle band, without anyone transmitting) less than S0? Hit `AMP1`. Is the noise floor still under S1? You are blessed - hit `AMP2`!!!! Otherwise, your noise floor already greater than S1? Use it in `IPO`.
* **CAVEAT:** I found amplifiers to be useful in digital modes, even with noise floor higher than S1. Also, remember that when you are amplifying a signal, you are *also amplifying the noise* - It will *hardly* make your target signal more audible! Counter-act with filters, RF Gain, something else - the preamp won't make the miracle happen. Also, don't use amplifiers with the [attenuator](#att) turned on, because... Well, defeats the purpose. If you see both `AMP` and `ATT` in the display, fix it!

# Page 2
Digital Signal Processing and filtering

| [NOTCH](#notch) | [CONT](#cont) | [DNR](#dnr) | [DNF](#dnf) |
| --- | --- | --- | --- |
| [<= BACK](#page-1) | **[SHIFT](#shift)** | **[WIDTH](#width)** | [FWD =>](#page-3) |

## NOTCH
* **WHAT:** This is a special kind of filter that blanks out a narrow part of a signal.
* **AVAILABLE OPTIONS:** Off, 10 to 3200 Hz. Use with "Multi" encoder.
* **RX or TX?** RX
* **WHICH MODE?** CW, SSB, AM
* **WHEN TO USE:** Very but *VERY* useful in digital modes. In phone mode, it is supplanted by the [DNF](#dnf) function (see link). Enable it to knock-out the interfering signal. Works better if you have a visualization of the interfering signal, otherwise you will have to seek turning the multi encoder until you get rid of the offending beat/signal.
* **CAVEAT:** This is **GREAT** to defend from a strong signal in FT-8! Check [this article](/rfrht/FT-991A/wiki/Using-FT-991A-Filters-to-Improve-your-FT-8-Reception). Ensure to have your menu setting `114 - IF Notch Width` set to `NARROW`.

## CONT
* **WHAT:** Contour is an Yaesu Special filter that differently from a Notch filter that kills an target signal, the contour only slightly attenuate around the target receiving audio frequency.
* **AVAILABLE OPTIONS:** Off, 10 to 3200 Hz. Use with "Multi" encoder.
* **RX or TX?** RX
* **WHICH MODE?** CW, SSB, AM
* **WHEN TO USE:** Do you know that strident audio from some operator? You can enable Contour filter, tune it around and make that signal sound a bit better and least harsh.
* **CAVEAT:** Not of super duper use in Digital modes. More useful in phone modes.

## DNR
* **WHAT:** This is one of the finest functions of this equipment: The Digital Noise Reducer. The task is performed by the radio's DSP (Digital Signal Processor) and the aim is to remove as much as possible the shhhhhhhhhhhhhh noise from a signal.
* **AVAILABLE OPTIONS:** Off, 1-15. Use with "Multi" encoder.
* **RX or TX?** RX
* **WHICH MODE?** AM, SSB, CW
* **WHEN TO USE:** Nice to make your receiving less tiring, getting rid of the regular band noise. The settings 1-15 are actually different DSP *programs*. Start with 1, stick to the one that yields the most comfortable receiving. Do *not* use in digital modes!
* **CAVEAT:** This is not an signal maker or an miraculous godsend: If the target signal is pretty marginal and close to the noise level, you will definitely hear the "bubblish" or "waterish" audio. Because, the DSP just doesn't have enough signal to filter out, it confounds the signal and noise level. The solution? [Check this article](/rfrht/FT-991A/wiki/FT-991A-DSP-and-DNR-performance), there are some tactics over here to help counteract interferences.

## DNF
* **WHAT:** Digital Noise Filter, AKA Autonotch, is one of my favourite functions of this radio. When enabled, it "listens" to what you are receiving, and if is there any beats / carrier / birdies / beep / tune, the DNF will intercept and kill that signal off. Automagically. Yea.
* **AVAILABLE OPTIONS:** On, Off
* **RX or TX?** RX
* **WHICH MODE?** AM, SSB, CW
* **WHEN TO USE:** Do you know those operators that likes tune over the active frequency? Yes, those uneducated and pesky ones. Just hit DNF and get rid of them. Like magic. Unfortunately, it can't zero out whistles. Dang.
* **CAVEAT:** UNLESS you have an constant interfering signal, you won't want the DNF on all the time - gives some kind of 'bottled' effect to the audio, due to the DSP scanning and trying to neutralize potential offending signals. So unless in need, keep it `OFF`.

## SHIFT
* **WHAT:** The shift function "shifts" (doh again) your receiving bandpass to above or below (or left or right), removing either the bass or treble part of the signal depending to the direction that you set the shift - narrowing the received signal.
* **AVAILABLE OPTIONS:** -1200 Hz to +1200 Hz.  `0` means no shift, disabled. Set with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** AM, SSB, CW
* **WHEN TO USE:** The primary use is to defend from an adjacent signal over the lower or higher edge of your receiving signal. Use shift to dodge this interfering signal.
* **CAVEAT:** This is also useful to make the receiving less tiring, irrespective of having or not an interfering signal - Try using Shift between `-600` and `-200` together with [DNR](#DNR) - I promise you will love it!

## WIDTH
* **WHAT:** Changes the receiving Audio/signal Bandpass. The larger, more detailed (or full, or rich, or heavy) the audio (and more interference too); the narrow, less detail, more strong on mid-level tones (and less interference) too.
* **AVAILABLE OPTIONS:** Varies with each mode. For example sake, in SSB in [Narrow](#narwide) mode goes from 200-1800 Hz, while in [Wide](#narwide) the bandpass goes from 1800-3200 Hz. Use with "Multi" encoder.
* **RX or TX?** RX
* **WHICH MODE?** SSB, CW, RRY/PSK
* **WHEN TO USE:** If you are receiving strong phone signals, you will want it as wide as possible. When working that challenging signal, move it to narrow and set a according bandwidth to the minimum copyable signal.
* **CAVEAT:** In CW mode you will want it as narrow as possible.

# Page 3
Miscellaneous 

| [MOX](#mox) | [VOX](#vox) | [APF](#apf) | [MONI](#moni) |
| --- | --- | --- | --- |
| [<= BACK](#page-2) | **[MIC-EQ](#mic-eq)** | **[PROC](#proc)** | [FWD =>](#page-4) |

## MOX
* **WHAT:** "Manual Operation Transmit" puts the radio in a locked transmission mode. It can be the poor's man remote PTT, hold the radio in transmit mode while you sweep the band checking the VSWR, etc.
* **AVAILABLE OPTIONS:** Off, On
* **RX or TX?** TX
* **WHICH MODE?** All modes
* **WHEN TO USE:** Testing, activating in long transmission ragchew so you don't have to hold PTT...
* **CAVEAT:** If you put the radio in Mox mode in SSB without modulating anything, it will transmit 0W power, because differently from CW, AM or FM, there's no carrier in SSB mode! So no talk, no power. You talk, you emit power. CW, FM or AM, conversely, will emit power, irrespective of having you talking or not - because those have actual carrier.

## VOX
* **WHAT:** "Voice Operator Transmit" is a very convenient mode - it will kick in the transmission automatically if it detects you talking. Conversely, it ends transmission if it audio ceases.
* **AVAILABLE OPTIONS:** Off, On
* **RX or TX?** TX
* **WHICH MODE?** All modes
* **WHEN TO USE:** That's for the lazy, and lazy is good. If you have an microphone close to you, and you don't want to bother on PTT, just enable Vox, start talking and the equipment does the magic. Be sure to configure it properly the trigger level in Menu `143 - Vox Gain` and the trailing grace period after you got muted in Menu `144 - Vox Delay`.
* **CAVEAT:** It is super useful for digital modes that doesn't have PTT control. You feed the audio, poof, the radio transmits. If you are feeding audio via the USB port, ensure to set the Menu `142 - Vox Select` to `Data`. [More details here](https://forums.qrz.com/index.php?threads/going-software-defined.650584/#post-5131572), check the "Radio Config" section (there's a number of other settings to be done too). Also ensure you don't have any nearby TV, stereo, other radios, your significant one (especially when picking up a fight or intimate moments) with Vox activated. Otherwise, you will certainly have assured audience.

## APF
* **WHAT:** Audio Peak Filter - This is an CW function that enables an very narrow filter, compared to the optional crystal filters, reducing the bandwidth to 100-300 hertz (configurable), wiping out unwanted/competing signals. If in CW mode and you have neighboring signals making hard your copy, APF comes to your rescue, removing everything else from neighboring sides.
* **AVAILABLE OPTIONS:** Off, -250 to +250
* **RX or TX?** RX
* **WHICH MODE?** CW
* **WHEN TO USE:** This should be an one-time setting, done in tandem with your preferred receiving CW signal [PITCH](#pitch). Define your preferred pitch, and then find the suitable APF setting, and you will be mostly just enabling and disabling it. 
* **CAVEAT:** It is of use if you have a default somewhat wide bandwidth so you can hunt for the signal of interest. Tune to the signal of interest, enable `APF` and turn the multi encoder until you "seize" the signal of interest - or just make your receiving more silent. The `APF` bandwidth is governed by Configuration clause `111 - APF Width`. The values are, namely:
    * Narrow: 100 Hz wide
    * Medium: 100 Hz wide
    * Wide: 300 Hz wide

## MONI
* **WHAT:** Monitor - plays back in audio output the actual audio that is being modulated and sent to the radio transmit block.
* **AVAILABLE OPTIONS:** Off, 0-100. Use with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** AM, SSB, Digital
* **WHEN TO USE:** The MONI function is very useful for check what you are actually putting the radio to transmit. So you can check how are you sounding, the equalization, the processor level, etc. The down point is that... Well, as you speak you don't have much of an ability to hear yourself properly. The 0-100 level sets how loud will be the feedback.
* **CAVEAT:** Use headphones - this will help a bit, instead of using the radio's speaker (which should be avoided, in my opinion - it sounds awful bad to my taste.). 

## MIC-EQ
* **WHAT:** Microphone Equalization.
* **AVAILABLE OPTIONS:** Off, On
* **RX or TX?** TX
* **WHICH MODE?** AM, SSB
* **WHEN TO USE:** On voice modes. This is one nice feature, but will require time and patience to get this set properly. Adjust your audio settings in Config Menu clauses `119` to `127`. EQ on, equalizer actuating as per the aforementioned configurations. EQ off, flat equalization, no audio transformation.
* **CAVEAT:** The best way to equalize your audio is to do it real time with an remote SDR over the web. So you adjust, you talk, and hear from the web SDR your signal. Use an headphone for best results!!! One gotcha: The MIC-EQ has no effect in audio fed by the rear RTTY/Data or USB port.

## PROC
* **WHAT:** Speech Processor
* **AVAILABLE OPTIONS:** Off, 1-99. Use with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** AM, SSB
* **WHEN TO USE:** Useful in phone modes. Adds "punch" or "talk power" to your modulation, by a number of audio processing techniques performed by the transceiver's DSP. If you are really curious how speech processors work, check [this datasheet](https://www.analog.com/media/en/technical-documentation/obsolete-data-sheets/SSM2165.PDF).
* **CAVEAT:** Too much compression is no good. Do your test audio transmission, set your [Meter](#meter) to `COMP`, tune the multi encoder to set the level and monitor the transmit bar - Ideally, this should be only *peaking* the -20dB position. Normally, it will be done with low values.

# Page 4
CW Functions

| [ZIN](#zin) | [SPOT](#spot) | [PITCH](#pitch) | [KEYER](#keyer) |
| --- | --- | --- | --- |
| [<= BACK](#page-3) | **[BK-IN](#bk-in)** | **[SPEED](#speed)** | [FWD =>](#page-5) |

## ZIN
* **WHAT:** Zero-In: Tune to the signal of interest
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** Tune function
* **WHICH MODE?** CW
* **WHEN TO USE:** Zero-In is an very useful function - When you find the signal that you are interested, hit `ZIN` and it will automatically tune the signal and set the [PITCH](#pitch) already configured for your preference.
* **CAVEAT:** When looking for signals (hunting), Disable [APF](#apf) and then when you find the signal of interest, hit `ZIN` and then enable `APF`.

## SPOT
* **WHAT:** Took time to understand this one. And this is clumsy, sheesh. Outputs a tone specified in [PITCH](#pitch), with the volume defined in [MONI](#moni), so you can use your ears to match the transmitting signal. Challenging.
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX
* **WHICH MODE?** CW
* **WHEN TO USE:** While not an CWer, when nearby the signal of interest (and if you have [MONI](#moni) set in a suitable number), hold `SPOT` while you tune so you can zero-in the transmitting signal. Something that [ZIN](#zin) does automatically. But... Well, go figure.
* **CAVEAT:** Spare yourself the hassle and use ZIN instead. If you really want to use it, ensure that you have [MONI](#moni) set in a suitable volume, otherwise you won't hear the tone when you push `SPOT`.

## PITCH
* **WHAT:** Defines your preferred CW pitch tone.
* **AVAILABLE OPTIONS:** Use with "Multi" encoder.
* **RX or TX?** RX and TX
* **WHICH MODE?** CW
* **WHEN TO USE:** This is likely something to be an one-time setting. Select your preferred `PITCH` tone while you key until you find your preferred tone.
* **CAVEAT:** After configuring your favourite pitch, find some signal of interest, hit [ZIN](#zin), enable the [APF](#apf) and configure the APF so the signal comes out strong with your desired pitch setting.

## KEYER
* **WHAT:** Toggles your CW encoder between regular key or iambic (keyer).
* **AVAILABLE OPTIONS:** On / Off
* **RX or TX?** TX
* **WHICH MODE?** CW
* **WHEN TO USE:** If you have an iambic paddle, set keyer to `On`. Otherwise if you have straight/standard key, leave it on `Off`.
* **CAVEAT:** Is your transceiver producing a series of beeps in your straight key? Set KEYER to `Off`! Your iambic paddle is only sending a continuous beep? Set KEYER to `On`!

## BK-IN
* **WHAT:** Binds your CW key to the transmit stage.
* **AVAILABLE OPTIONS:** Off, On
* **RX or TX?** TX
* **WHICH MODE?** CW
* **WHEN TO USE:** You can actually use your transceiver to practice/test CW! Set BK-IN mode to `Off` and you will hear the beep feedback normally, without transmitting. When you are good to transmit, mark it `On` and then it will transmit your code.
* **CAVEAT:** Are you encoding and the radio is not transmitting? Check BK-IN and move it from `Off` to `On`!

## SPEED
* **WHAT:** Defines the [Keyer](#keyer) encoding speed in words per minutes (WPM).
* **AVAILABLE OPTIONS:** 4 - 60 WPM. Use with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** CW
* **WHEN TO USE:** Only relevant if you have enabled the built-in [Keyer](#keyer) and have it in iambic mode.
* **CAVEAT:** ---

# Page 5
Power & Gain Settings

| [METER](#meter) | [RF PWR](#rf-pwr) | [MIC GAIN](#mic-gain) | [SWEEP](#sweep) |
| --- | --- | --- | --- |
| [<= BACK](#page-4) | **[DT GAIN](#dt-gain)** | **[CH DIAL](#ch-dial)** | [FWD =>](#page-6) |

## METER
* **WHAT:** This function changes the meter measurements during a transmission. Scale of interest in bottom side of the meter. **Only** during transmission, because during reception the radio stays in S-meter (scale in the upper side of the meter).
* **AVAILABLE OPTIONS:** Below are the options:
    * PO - Power output
    * ALC - Automatic Level Control.
    * SWR - Standing Wave Ratio
    * COMP - Speech processor compression level
    * IDD - TX stage current draw
    * VDD - TX stage voltage
* **RX or TX?** TX
* **WHICH MODE?** All modes
* **WHEN TO USE:** During transmissions :-)
* **CAVEAT:** A few notes about meters:
    * ALC - It is constant in FM, C4FM, AM and CW modes. It is very useful for SSB phone or digital modes. For SSB Phone, you will want the ALC level as ahead as possible inside the blue bar (ends around S9), without letting it move more than +10. Adjust it using the [MIC GAIN](#mic-gain) using your average voice for proper ALC level. For your digital modes, you will get more success on sending your signals with ALC between S2-4. *Remember to monitor your ALC level in digital modes!*
    * COMP - Use it when calibrating the [Processor Gain](#proc). Let peaks reach 20dB, don't let exceed.

## RF PWR
* **WHAT:** Transmit Power
* **AVAILABLE OPTIONS:** 5-100W HF-6m (AM: 40W); 5-50W 144 & 430. Use with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** All modes
* **WHEN TO USE:** Set the proper transmit power.
* **CAVEAT:** Monitor your TX power in tandem with ALC. If ALC is way back, that means that the transceiver is underdriven and will not yield the power level that you have set up, Needing more gain (adjust [MIC GAIN](#mic-gain)) - or SWR too high! Ensure to [monitor](#meter) it properly.

## MIC GAIN
* **WHAT:** Front Mic port gain
* **AVAILABLE OPTIONS:** 1-100. Use with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** All modes but CW
* **WHEN TO USE:** In SSB, use it in tandem with [ALC](#meter) monitor, keeping the ALC within the blue range, peaking or slightly exceeding at the right end of the ALC scale (there's a blue bar below the meter when in ALC mode). Check the link reference for proper Mic gain level.
* **CAVEAT:** You might have different mic gain levels for data modes, SSB, FM or even different bands.

## SWEEP
* **WHAT:** Ah, the pesky sweep. This controls the spectrum waterfall. Keep reading.
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX
* **WHICH MODE?** All modes
* **WHEN TO USE:** If you touch it quickly, it will stop the signal waterfall. To resume it, push and hold until you hear two beeps.
* **CAVEAT:** If your waterfall is stuck, it is because you probably hit by accident (or tried) the Sweep button accidentally. Push and hold it to resume your signal waterfall.

## DT GAIN
* **WHAT:** Similarly from [MIC GAIN](#mic-gain), this functionality controls the gain in the rear ports of the radio: The RTTY/Data DIN connector or the USB port. Those are controlled by DT GAIN.
* **AVAILABLE OPTIONS:** 1-100. Use with "Multi" encoder.
* **RX or TX?** TX
* **WHICH MODE?** All modes but CW
* **WHEN TO USE:** If you are using SSB Digital modes, use it in tandem with [ALC](#meter) monitor.
* **CAVEAT:** If you feed your voice audio from the rear USB coming from a computer, this is where you should adjust the gain, instead of [Mic Gain](#mic-gain)

## CH DIAL
* **WHAT:** One of my hottest and favourite: Super fast tuning using the Multi encoder
* **AVAILABLE OPTIONS:**
    * SSB, CW: 1 kHz, 2.5 kHz, 5 kHz
    * FM, C4FM: 5 kHz, 6.25 kHz, 10 kHz, 12.5 kHz, 15 kHz, 20 kHz, 25 kHz
    * AM: 2.5 kHz, 5 kHz, 9 kHz, 10 kHz, 12.5 kHz, 25 kHz
* **RX or TX?** Tune function
* **WHICH MODE?** All modes
* **WHEN TO USE:** I like tuning around in HF band using the CH Dial function, usually in 1 or 5 kHz step instead of the main VFO. Quicker movement. Push CH.DIAL, your display will show the `CH-D` indication and turn the encoder to tune to the desired signal.
* **CAVEAT:** If you enable the `FAST` function in the radio, the steps are multiplied by 10.

# Page 6
Ancillary Tuning options

| [HOME](#home) | [SQL](#sql) | [MCH](#MCH) | [GRP](#grp) |
| --- | --- | --- | --- |
| [<= BACK](#page-5) | **[DEC/DEL](#decdel)** | **[SCAN](#scan)** | [FWD =>](#page-7) |

## HOME
* **WHAT:** Recalls the Home frequency to the VFO
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** Tune function
* **WHICH MODE?** All modes
* **WHEN TO USE:** This serves as a shortcut for recalling an favourite frequency. Hit `HOME` and your radio moves back to it.
* **CAVEAT:** How do you set the Home Frequency:
    1. Push the `HOME` button
    2. Push the `BAND` rubber button and select the `ENT` (lower right corner of display)
    3. Type the desired frequency and hit `ENT`

## SQL
* **WHAT:** That controls the squelch level.
* **AVAILABLE OPTIONS:** 0-100. Use with "Multi" encoder.
* **RX or TX?** RX
* **WHICH MODE?** All Modes
* **WHEN TO USE:** Mostly in AM or FM. In SSB usually you leave it in `0` setting, because... Well, QSB.
* **CAVEAT:** If your squelch level is too tight, you may not be able to receive C4FM! Ensure that the squelch is adjusted sufficiently to open in the presence of the C4FM signal.

## MCH
* **WHAT:** Sets the Multi Encoder to scroll **Memory** channels
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** Tune function
* **WHICH MODE?** All modes
* **WHEN TO USE:** Pay attention here.
    1. Use only if you have memories set in your equipment;
    2. If you have memories and want to scroll them, **first enter the Memory mode** by pushing the `V/M` rubber button.
    3. And then use the encoder to scroll throught the memories.
* **CAVEAT:** If your radio has the `MCH` mode active (see in display), you are in VFO mode (instead of memory) and you turn the Multi encoder, expect for a pain in the ass. To exit this mode, press the `F M-List` button and set the multi to something else, like [CH Dial](#ch-dial), otherwise it will get back to presenting a list of channels in the display when you turn the Multi encoder.

## GRP
* **WHAT:** Sets the Multi Encoder to scroll Memory *groups*
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** Tune function
* **WHICH MODE?** All modes
* **WHEN TO USE:** If you make use of memory groups (manual page 110), by entering the GRP mode, your encoder will scroll through the 7 memory groups of the radio: Memories 01, 20, 40, 60, 80 and the 60-m band, so you can use the [MCH](#mch) function and scan within the group limits.
* **CAVEAT:** Be sure to consult your manual page 110 to fully understand the memory groups. In order to enable (and use) it, you must have the Configuration Clause `034 - Mem Group` to `ENABLE`. Do not enable it if you don't fully understand memory groups; please do an manual detour first.

## DEC/DEL
* **WHAT:** Decrease the Contest Number in automated CW messages
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX/TX
* **WHICH MODE?** CW
* **WHEN TO USE:** If you use CW pre-baked text messages for contests and you missed a contact or want to roll back the serial number, push the `DEC/DEL` button to rollback the last contact and decrease one from the serial number.
* **CAVEAT:** The current serial number is depicted in Configuration Clause `017 - CONTEST NUMBER`. Every time you press `DEC/DEL` you decrease one from that number. Learn more about CW automated messages using the [CH1-5](#ch1-5) in manual Page 86 and on.

## SCAN
* **WHAT:** Engages scan mode.
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX
* **WHICH MODE?** All modes
* **WHEN TO USE:** If you want to scan the band or the memories for activity
* **CAVEAT:** If you are in [MCH](#mch) mode and hit scan, the scan will be performed in the memories. Exit `MCH` if you want to scan the band. Ensure to set a proper [Squelch](#SQL) level for an enjoyable scan.

# Page 7
FM Functions

| [RPT](#rpt) | [REV](#rev) | [SQL OFF](#sql-off) | [T.CALL](#tcall) |
| --- | --- | --- | --- |
| [<= BACK](#page-6) | **[TONE/DCS](#tonedcs)** | **[MUTE](#mute)** | [FWD =>](#page-8) |

## RPT
* **WHAT:** Selects the transmit frequency shift (above or below frequency) for proper repeater configuration.
* **AVAILABLE OPTIONS:** Simp, +, -
* **RX or TX?** TX
* **WHICH MODE?** FM, C4FM
* **WHEN TO USE:** This option is used when using the radio to hit an repeater. Usually, repeaters needs an upper or lower TX frequency offset, so the repeater gets your signal in this different uplink frequency and then spreading (well, repeating) in the repeater main output frequency.
* **CAVEAT:** The frequency shift is governed by standard values - and your 991A is aware of these frequency/shift pairs and can automatically calculate it. This is named *ARS - Automatic Repeater Shift*. If you set your radio configurations `084` and `085` to `On`, then the radio automatically calculates the proper transmit shift frequency.

## REV
* **WHAT:** Listen to **Reverse** Frequency
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX
* **WHICH MODE?** FM, C4FM
* **WHEN TO USE:** Use this functionality to check the repeater's uplink frequency - Use it to (try to) hear what the other party is actually transmitting to the repeater.
* **CAVEAT:** Some examples: if you can hear someone transmitting in the uplink frequency, so you can determine if the fellow chap is nearby, or check the other party modulation to the repeater, etc. Only of use if you are using a repeater shift (+ or -). It is of no use if you are in simplex mode, because... The TX and RX frequency are the same. <grins>

## SQL OFF
* **WHAT:** Temporarily set your squelch to zero, opening the receiving audio
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX
* **WHICH MODE?** All modes
* **WHEN TO USE:** Useful when you are using squelched audio. Push the button and the squelch opens and you hear the audio, without having to reprogram the squelch level.
* **CAVEAT:** Especially useful when you are receiving an mobile station or something with an variable signal - and you don't have time/want to reprogram your squelch level.

## T.CALL
* **WHAT:** Sends an 1750 Hz Tone call
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** TX
* **WHICH MODE?** FM
* **WHEN TO USE:** Some repeaters requires an 1750 tone before you transmit, in order to arm the repeater. Hit `T.CALL` so the radio can activate the remote repeater.
* **CAVEAT:** This is something more common in European continent. Do not mistake with CTSS/DCS tone, this is an entirely different animal.

## TONE/DCS
* **WHAT:** Controls Tone/DCS encoding or RX squelch
* **AVAILABLE OPTIONS:** A number of options:
    1. **Off** - No tone/code encoding or decoding
    2. **ENC** - *Transmission only* - Encodes the configured CTSS [Tone](#tone) along your transmission for proper remote squelch. Very used in FM repeaters.
    3. **CTCSS** - *Receiving only* - Only open the radio squelch if the incoming/receiving signal matches the configured CTSS [Tone](#tone) setting. Useful if you have a friend and you guys have combined an specific tone for your conversation - So when the received signal has the specified the tone, your radio opens squelch and outputs the other party signal. Otherwise, the radio remain silent, even in the presence of signal.
    4. **D.ENC** - *Transmission only* - Encodes the configured [DCS](#dcs) code along your transmission for proper remote squelch. Very used in FM repeaters.
    5. **DCS** - *Receiving only* - Only open the radio squelch if the incoming/receiving signal matches the configured [DCS](#dcs) code setting. Useful if you have a friend and you guys have combined an specific DCS code for your conversation - So when the signal matches the code, your radio opens squelch and outputs the other party signal.
* **RX or TX?** RX and TX
* **WHICH MODE?** FM
* **WHEN TO USE:** Explained in each option.
* **CAVEAT:** This is the cause of lots of complaints of "My radio is mute in 2 meter band" or "I can't receive in FM mode" - You probably have set either `CTCSS` or `DCS` modes. Disable (`OFF`) or set it accordingly.

## MUTE
* **WHAT:** Quickly mute the receiving signal
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX
* **WHICH MODE?** All modes
* **WHEN TO USE:** Hit the Mute button if you find inconvenient to just reduce the main radio volume.
* **CAVEAT:** I really can't find much of use of this functionality, what to say about caveats...

# Page 8
C4FM & Encoding functions

| [GM](#gm) | [AMS](#ams) | [X](#x) | [DIGITAL](#digital) |
| --- | --- | --- | --- |
| [<= BACK](#page-7) | **[TONE](#tone)** | **[DCS](#dcs)** | [FWD =>](#page-9) |

## GM
* **WHAT:** 
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** 
* **WHICH MODE?** C4FM
* **WHEN TO USE:** 
* **CAVEAT:** 

## AMS
* **WHAT:** The AMS function enables or disables the "Auto Mode Set". What does that mean? Let a hybrid repeater, Analog & C4FM. With the AMS setting to `ON`, the radio will detect what's the signal type, C4FM or analog. During C4FM reception the radio decodes normally the audio stream. Now, if the incoming signal is a regular analog transmission, the radio will output the analog audio on the speakers. With the AMS `OFF`, the radio does not output in other streams than C4FM and stays silent.
* **AVAILABLE OPTIONS:** On, Off
* **RX or TX?** RX
* **WHICH MODE?** C4FM
* **WHEN TO USE:** If you have a hybrid Analog and C4FM repeater leave it on. Otherwise, set it to off.
* **CAVEAT:** If you have a hybrid **digital** repeater, like C4FM and DMR / D-Star- Set the AMS to off, otherwise it will output the other protocol's digital transmission - and it's unpleasant.

## X
* **WHAT:** Enables / Disables the Wires-X functionality. Wires-X is a very fine functionality that allows you to join other channels, and even rooms bridged with other networks such as DMR or D-Star. Requires a repeater with proper support.
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** RX, TX
* **WHICH MODE?** C4FM
* **WHEN TO USE:** When using a C4FM repeater, hit the X button to enable the Wires-X functionality. After the connection is established, push `SEARCH & DIRECT` button. If you are not presented a numeric keypad, push the `ID` button - and finally, type the 5-number code of your desired room.
* **CAVEAT:** Check [this directory](https://register.ysfreflector.de/) for C4FM/Fusion/Wires-X rooms. Use the "ID" field.

## DIGITAL
* **WHAT:** This option controls the C4FM encoding schema.
* **AVAILABLE OPTIONS:** DN, VW
* **RX or TX?** TX
* **WHICH MODE?** C4FM
* **WHEN TO USE:** The DN mode halves the total C4FM bandwidth, reserving half of it for audio and the other half for data and control. The `VW` mode provides a (zomg I hate this term) "Richer audio", while the `DN` mode is needed for repeater usage, because of the needed data and control that makes goes through the data channel.
* **CAVEAT:** IF you are using a repeater or Wires-X, use the `DN` mode. Repeater won't work in `VW` mode. If you are ragchewing on simplex with a friend in C4FM mode, use the `VW` mode for better audio quality.

## TONE
* **WHAT:** Defines the CTSS tone to be encoded or decoded in function [TONE/DCS](#tonedcs)
* **AVAILABLE OPTIONS:** All standard tones, from `67.0 Hz` to `254.1 Hz`. Use with "Multi" encoder.
* **RX or TX?** RX and TX
* **WHICH MODE?** FM
* **WHEN TO USE:** This is used in conjunction with the [TONE/DCS](#tonedcs) setting, defining the CTSS tone to be encoded or the tone to be received and open squelch.
* **CAVEAT:** --

## DCS
* **WHAT:** Defines the DCS Code to be encoded or decoded in function [TONE/DCS](#tonedcs)
* **AVAILABLE OPTIONS:** DCS codes from `023` to `754`. Use with "Multi" encoder.
* **RX or TX?** RX and TX
* **WHICH MODE?** FM
* **WHEN TO USE:** Also, this setting is used in conjunction with the [TONE/DCS](#tonedcs) setting, defining the DCS code to be encoded or the code to be received and open squelch.
* **CAVEAT:** ---

# Page 9
Record & playback pre-recorded messages

| [CH1](#ch1-5) | [CH2](#ch1-5) | [CH3](#ch1-5) | [CH4](#ch1-5) |
| --- | --- | --- | --- |
| [<= BACK](#page-8) | **[CH5](#ch1-5)** | **[MEM](#mem)** | [FWD =>](#page-10) |

## CH1-5
* **WHAT:** Plays an previously recorded message.
* **AVAILABLE OPTIONS:** Push Buton
* **RX or TX?** TX
* **WHICH MODE?** CW, SSB, AM
* **WHEN TO USE:** This is a useful tool to play repetitive messages, like CQ, reports, etc.
* **CAVEAT:** You can get the feedback by enabling the [MONI](#moni) function. Also, you will only actually transmit if you have the [BK-IN](#bk-in) in `ON` state. With BK-IN off, you will only hear the playback without transmitting (*if* you have enabled MONI and in a suitable volume). These playbacks are also done by the Remote Control unit FH-2. **IF** you are into the Do-It-Yourself, instead of coughing around $100 in a new one, you can build yours for less than $10 - [Check this project](https://github.com/rfrht/RFH-2).

## MEM
* **WHAT:** Records a new message for [CH 1-5](#ch1-5) buttons
* **AVAILABLE OPTIONS:** Push Button
* **RX or TX?** --
* **WHICH MODE?** CW, SSB, AM
* **WHEN TO USE:** Hit the `MEM` button and then the desired [CH 1-5](#ch1-5) button to assign a voice message to that button.
* **CAVEAT:** To start the recording, hold PTT. To end the recording, push the `MEM` button. You are limited to 20 seconds for each button.

# Page 10
Bottom Row Configuration Menu

| [SWAP F1](#swap-f1-f4) | [SWAP F2](#swap-f1-f4) | [SWAP F3](#swap-f1-f4) | [SWAP F4](#swap-f1-f4) |
| --- | --- | --- | --- |
| [<= BACK](#page-9) |  |  | [FWD =>](#page-1) |

## SWAP F1-F4
* **WHAT:** Reprograms the bottom button row of your transceiver to any function you like!
* **AVAILABLE OPTIONS:** Push button
* **RX or TX?** --
* **WHICH MODE?** All Modes
* **WHEN TO USE:** *Do not miss it!* This is a handy function that will enable you to have four of your most favourite and useful functions at your reach in the bottom row of the menu! Just hit the button, the bottom row button will start flashing, find your desired function, push it and poof - it will show in the bottom line. Simple as that. A MUST.
* **CAVEAT:** Each mode (C4FM, CW, SSB, FM, AM) has its own setting for the bottom row! Be sure to customize the bottom row with the most used settings by you in each mode! For example, in FM I have [Meter](#meter), [Vox](#vox), [MCH](#mch) and [Scan](#scan). In SSB on the other hand, I have [Meter](#meter), [Ch Dial](#ch-dial), [Vox](#vox) and [DNR](#dnr).

![Yaesu FT-991A Menu Settings](https://rf3.org:8443/q/wink-menus.png)
