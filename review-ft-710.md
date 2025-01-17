# Review: Yaesu FT-710 under the perspective of a FT-991A user. (WIP)
## Introduction
I've been a [happy FT-991A user](https://github.com/rfrht/FT-991A/wiki/Review-FT-991A) since 2019. And now... The FT-710. I started writing this review with a bit less than a month operating the FT-710. Here are my ramblings.

## Why a FT-710?
First and beforehand - because the FTDX-10 was outside my budget. It would have been it. But, why a new radio, wasn't FT-991A good enough? Sure, it is. I'm severely limited **by the antenna and my local noise**, not the radio. However, I wanted another radio so I could operate the 991A in VHF/UHF and the new radio on HF band. Simultaneously. And I wanted a new and capable HF radio, just because.

## Operating
Face it, you get used to your default rig. There's an entirely new operation paradigm in the FT-710 - and [takes time and effort to adapt](https://github.com/rfrht/PY2RAF/blob/master/Improving-FT-710-usability.md). So, no longer hundreds of config clauses under a single "Setup" block, multiple menu pages, nope: it now have a few key fixed operating aspects in the "menu" page and specific configurations are now grouped on functionalities in a submenu-like structure. That made sense, in my opinion. And no, it's no Icom's icon user experience design (UXD).

Out of the box, the radio ships a [new microphone, model SSM-75E](https://www.eham.net/reviews/view-product?id=15065) with some function buttons on it. I'm yet to play with it, but it's a departure from the [classic MH-31](https://www.universal-radio.com/catalog/hamhf/0406FT900.html) and adds shortcuts at your fingertip. Again, to be explored in the future. I found the mic audio to be muffled especially when using BW 200-2900. That said, when operating with the PTT I shrank the BW to 300-2700 Hz. 200-2900 only when operating via the Sennheiser headset. There's no switch like MH-31 where you can select the bandwidth.

CAT-wise, it is _fairly_ compatible with the FT-991A command set on the **base** functionality. Don't take it for granted, and if you use scripts, test them all - and fix it. Chances are big that you will find a non-trivial amount of commands to be rewritten. The `EX` command series are entirely different.

I miss a dedicated Clarifier/RIT button, and I wish I could configure the CLAR button to on-off, instead of toggling it through `CLAR RX`, `CLAR TX`, `CLAR TX/RX` and finally `CLAR OFF` to get it off.

I found a small bug; when the radio is on `SQUELCH - FM ONLY`, the `SQL` pin 6 on the RTTY/DATA rear port (I use it on my [timer](https://github.com/rfrht/Yaesu-OLED-TX-Timer)) stays asserted - even when the radio receiving. I'm yet to report this bug to Yaesu.

And now, the DSP - zommmmggg the DSP. The DNR function is so capable (choose the right DNR setting by pressing and holding the button) to the point to actually **help** weak signals. I used the DNR on my 991A only with very strong signals. On FT-710, it helps with weak signals too. Very good.

With regards to the sensitivity - I leave my RX S-Meter in a point that in idle band it **swings** between 0-3 S-Units. So in 40M band, with the FT-991A with a clean front-end (IPO, no attenuator) I had a S2-S3 noise floor. With the 710 - this is where it blows the 991A out of water - IPO gets me to S8-9! So yes, now I have to run it attenuated, varying between 6 and 12 dB of attenunation. Damn big ears. If I lived in a RF-silent place, it would have resulted **net new contacts** due to the **very noticeable** extra sensitivity. However, as per the opening statements, I'm limited by my antenna constraints and a metropolitan area noise floor.

I also found that the radio runs significantly cooler than the FT-991A. In 991, when hitting PTT in VHF/UHF the fan would almost instantly kick in and accelerate, to the screaming level. I found that the 710 fan *seems* to have two stages: on and off. While on, is pretty much quiet (though not silent). I'm yet to find if the fan has more aggresive stages, but after some minutes-long SSB transmissions, the radio seemed to be unimpressed.

I have rewritten my [VoiceMeeter macros](https://github.com/rfrht/Voicemeeter-FT-991A/wiki) (in a [detached branch](https://github.com/rfrht/Voicemeeter-FT-991A/tree/RF)) and now I toggle between which radio I'm operating. There was a need for tweak the USB gain - and the mic gain, plus the AMC settings to have everything pretty much in harmony.

The scope is super eye candy, and departing from FT-991A, it's a balm. It improved significantly my operation ergonomy/experience and while I'm entertaining the idea of cracking open the radio and deploy a panadapter on it, so far what I got on the screen is more than enough - and useful - for me. Didn't like a lot the 3DSS thing, just using in the plain panadapter mode.

## Epilogue
Well, I sold my FT-710. Not because it was a bad radio; no, by no means: It was an awesome one. Lended to a friend during the holiday season, he got enchanted by the radio - it found a good home, a great operator, and it was a win-win. Didn't really need another radio, it was more a craving for new equipment - duly satisfied. Back to my FT-991A.
